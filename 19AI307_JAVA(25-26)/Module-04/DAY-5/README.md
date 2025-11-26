# Ex.No:4(D) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:
Create an Article class where changes to the content are saved as mementos. Let the user view and restore any saved version.

## AIM:
To implement the Memento Pattern for an Article, allowing saving, viewing, and restoring previous versions of its content.

## ALGORITHM :
1.	Start the program and create an Article object and an ArticleHistory manager.
2. Read the number of versions to save and the content for each version from the user.
3. Set the content of the article and save each version as a memento in ArticleHistory.
4. Read the index of the version to restore.
5. Retrieve the corresponding memento and restore the article’s content.
6. Display the restored content or show a message if the version index is invalid.





## PROGRAM:
 ```
/*
Program to implement a Behaviour Pattern using Java
Developed by: HAMZA FAROOQUE
RegisterNumber:  212223040054
*/
```

## SOURCE CODE:
```JAVA
import java.util.*;

class Article {
    private String content;

    public void setContent(String content) {
        this.content = content;
    }

    public String getContent() {
        return content;
    }

    public ArticleMemento save() {
        return new ArticleMemento(content);
    }

    public void restore(ArticleMemento memento) {
        this.content = memento.getContent();
    }
}

class ArticleMemento {
    private final String content;

    public ArticleMemento(String content) {
        this.content = content;
    }

    public String getContent() {
        return content;
    }
}

class ArticleHistory {
    private List<ArticleMemento> versions = new ArrayList<>();

    public void saveVersion(Article article) {
        versions.add(article.save());
    }

    public ArticleMemento getVersion(int index) {
        if (index >= 0 && index < versions.size()) {
            return versions.get(index);
        }
        return null;
    }
}

public class ArticleManager {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Article article = new Article();
        ArticleHistory history = new ArticleHistory();

        int n = Integer.parseInt(sc.nextLine());
        for (int i = 0; i < n; i++) {
            String content = sc.nextLine();
            article.setContent(content);
            history.saveVersion(article);
        }

        int restoreIndex = Integer.parseInt(sc.nextLine());
        ArticleMemento m = history.getVersion(restoreIndex);
        if (m != null) {
            article.restore(m);
            System.out.println(article.getContent());
        } else {
            System.out.println("Invalid version");
        }

        sc.close();
    }
}
```






## OUTPUT:


<img width="1212" height="639" alt="image" src="https://github.com/user-attachments/assets/dd5cafa0-fdc3-4871-b98a-07fc9849d5b6" />


## RESULT:
The program executed successfully and allowed the user to save multiple versions of an article and restore any previous version using the Memento Pattern.
