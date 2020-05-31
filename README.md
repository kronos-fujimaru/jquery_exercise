# jQuery 演習問題

Eclipse上に jquery_exerciseプロジェクトを作成して課題に取り組んでください。

<br>

## 演習1

jQueryで以下のような動作をする画面を作成しなさい。

【ページ読み込み時】
- h3要素のフォント色を赤にする。
- h3要素の背景色を黄色にする。

<br>

**jquery1.jsp**

```html
<%@ page language="java" contentType="text/html; charset=UTF-8"
    pageEncoding="UTF-8"%>
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>jQuery演習</title>
<script src="https://code.jquery.com/jquery-3.3.1.slim.min.js"></script>
<script type="text/javascript">
$(function() {
    // TODO
});
</script>
</head>
<body>
    <h1>jQuery演習</h1>
    <h2>jQuery演習</h2>
    <h3>jQuery演習</h3>
</body>
</html>
```

<br>
<hr>

## 演習2

jQueryで以下のような動作をする画面を作成しなさい。

【ページ読み込み時】
- テキストボックスに「Hello jQuery!」という文字列を入れる。

<br>

**jquery2.jsp**

```html
<%@ page language="java" contentType="text/html; charset=UTF-8"
    pageEncoding="UTF-8"%>
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>jQuery演習</title>
<script src="https://code.jquery.com/jquery-3.3.1.slim.min.js"></script>
<script type="text/javascript">
$(function() {
    // TODO
});
</script>
</head>
<body>
    <h1>jQuery演習</h1>
    テキスト：<input type="text" id="sample">
</body>
</html>
```

<br>
<hr>

## 演習3

jQueryで以下のような動作をする画面を作成しなさい。

【ページ読み込み時】
- ul要素（リスト）の中にli要素で「Apple」「Banana」「Cherry」を入れる。

<br>

**jquery3.jsp**

```html
<%@ page language="java" contentType="text/html; charset=UTF-8"
    pageEncoding="UTF-8"%>
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>jQuery演習</title>
<script src="https://code.jquery.com/jquery-3.3.1.slim.min.js"></script>
<script type="text/javascript">
$(function() {
    // TODO
});
</script>
</head>
<body>
    <h1>フルーツ一覧</h1>
    <ul id="fruits">
    </ul>
</body>
</html>
```

<br>
<hr>

## 演習4

jQueryで以下のような動作をする画面を作成しなさい。

【追加ボタンクリック時】
- テキストボックスに入力された値をul要素（リスト）に追加する。
- テキストボックスの値をクリアする。

<br>

**jquery4.jsp**

```html
<%@ page language="java" contentType="text/html; charset=UTF-8"
    pageEncoding="UTF-8"%>
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>jQuery演習</title>
<script src="https://code.jquery.com/jquery-3.3.1.slim.min.js"></script>
<script type="text/javascript">
$(function() {
    // TODO
});
</script>
</head>
<body>
    <h1>フルーツ一覧</h1>
    <ul id="fruits-list">
        <li>Apple</li>
        <li>Banana</li>
        <li>Cherry</li>
    </ul>
    <input type="text" id="fruit">
    <button id="add-fruit">追加</button>
</body>
</html>
```

<br>
<hr>

## 演習5

jQueryで以下のような動作をする画面を作成しなさい。

【追加ボタンクリック時】
- テキストボックス（フルーツ名、産地、価格）に入力された値をテーブルに追加する。
- すべてのテキストボックスの値をクリアする。

<br>

**jquery5.jsp**

```html
<%@ page language="java" contentType="text/html; charset=UTF-8"
    pageEncoding="UTF-8"%>
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>jQuery演習</title>
<script src="https://code.jquery.com/jquery-3.3.1.slim.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.7/umd/popper.min.js"></script>
<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.2.1/css/bootstrap.min.css">
<script type="text/javascript">
$(function() {
    // TODO
});
</script>
</head>
<body>
    <div class="container">
        <div class="row">
            <div class="col-8">
                <h1>フルーツ一覧</h1>
                <table id="fruits-list" class="table table-hover">
                    <tr>
                        <th>商品名</th>
                        <th>産地</th>
                        <th>価格</th>
                    </tr>
                    <tr><td>Apple</td><td>青森県</td><td>200円</td></tr>
                    <tr><td>Banana</td><td>フィリピン</td><td>100円</td></tr>
                    <tr><td>Cherry</td><td>山形県</td><td>500円</td></tr>
                </table>
                <br>
                フルーツ名：<input type="text" id="name" class="form-control w-50">
                産地：<input type="text" id="origin" class="form-control w-50">
                価格：<input type="number" id="price" class="form-control w-50"><br>
                <button id="add-fruit" class="btn btn-primary">追加</button>
            </div>
        </div>
    </div>
</body>
</html>
```

<br>
<hr>

## 演習6

jQueryで以下のような動作をする画面を作成しなさい。

【ボタン（Amazon、Google、Apple）クリック時】
- [サイトへ]リンクの遷移先URLに、各ボタンの企業に関するURLを設定する。
    - Amazon -> https://www.amazon.co.jp/
    - Google -> https://www.google.co.jp/
    - Apple -> https://www.apple.com/jp/
- クリックしたボタンのクラスに「btn btn-primary」を設定する。
- クリックしたボタン以外のボタンのクラスに「btn btn-light」を設定する。

<br>

**jquery6.jsp**

```html
<%@ page language="java" contentType="text/html; charset=UTF-8"
    pageEncoding="UTF-8"%>
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>jQuery演習</title>
<script src="https://code.jquery.com/jquery-3.3.1.slim.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.7/umd/popper.min.js"></script>
<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.2.1/css/bootstrap.min.css">
<script type="text/javascript">
$(function() {
    // TODO
});
</script>
</head>
<body>
    <div class="container">
        <div class="row">
            <div class="col-8">
                <h1>リンク</h1>
                <a id="site" href="#">サイトへ</a><br><br>
                <button id="amazon" class="btn btn-light" value="https://www.amazon.co.jp/">Amazon</button>
                <button id="google" class="btn btn-light" value="https://www.google.co.jp/">Google</button>
                <button id="apple" class="btn btn-light" value="https://www.apple.com/jp/">Apple</button>
            </div>
        </div>
    </div>
</body>
</html>
```

<br>
<hr>

## 演習7

演習6（jquery6.jsp）に以下のような動作を追加しなさい。

【[サイトへ]リンククリック時】
- [サイトへ]リンクの遷移先URLが「#」の場合は、「アクセスするサイトを選択してください。」のアラートを表示し、リンクが機能しないようにする。

<br>
<hr>

## 演習8

jQueryで以下のような動作をする画面を作成しなさい。

【ログインボタンクリック時】
- テキストボックスに入力されたログインIDが「user01」、パスワードが「pass01」の場合、メッセージ用のdiv要素にBootstrapのアラート（alert-primary）を用いて、「ログインに成功しました。」と表示する。
- 上記以外の場合、メッセージ用のdiv要素にBootstrapのアラート（alert-danger）を用いて、「ログインIDまたはパスワードに誤りがあります。」と表示する。

<br>

**jquery7.jsp**

```html
<%@ page language="java" contentType="text/html; charset=UTF-8"
    pageEncoding="UTF-8"%>
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>jQuery演習</title>
<script src="https://code.jquery.com/jquery-3.3.1.slim.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.7/umd/popper.min.js"></script>
<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.2.1/css/bootstrap.min.css">
<script type="text/javascript">
$(function() {
    // TODO
});
</script>
</head>
<body>
    <div class="container">
        <div class="row">
            <div class="col-8">
                <h1>ログイン画面</h1>
                <div id="message"></div>
                ログインID：<input type="text" id="id" class="form-control w-50">
                パスワード：<input type="password" id="password" class="form-control w-50"><br>
                <button id="login" class="btn btn-primary">ログイン</button>
            </div>
        </div>
    </div>
</body>
</html>
```

<br>
<hr>

## 演習9

jQueryで以下のような動作をする画面を作成しなさい。

【追加ボタンクリック時】
- 非同期通信（Ajax）を用いて、テキストボックスに入力されたフルーツ情報（フルーツ名、産地、価格）をexampleデータベースのfruitテーブルに登録する。
- 非同期通信が成功したら、以下の処理をする。
    - テキストボックス（フルーツ名、産地、価格）の値をHTMLのテーブルに追加する。
    - すべてのテキストボックスの値をクリアする。
    - メッセージ用のdiv要素にBootstrapのアラート（alert-primary）を用いて、「フルーツを追加しました。」と表示する。
- 非同期通信が成功したら、以下の処理をする。
    - メッセージ用のdiv要素にBootstrapのアラート（alert-danger）を用いて、「フルーツの追加に失敗しました。」と表示する。

> サーブレット（AddFruitServlet）を新規作成し、DAOとJSPのTODOの部分を埋めてください。<br>また、コネクションプールでDB接続をしてください。

<br>

**FruitDao.java（パッケージ：com.exercise.dao）**

```java
package com.exercise.dao;

import java.sql.Connection;
import java.sql.PreparedStatement;
import java.sql.ResultSet;
import java.sql.SQLException;
import java.util.ArrayList;
import java.util.List;
import javax.naming.NamingException;

import com.exercise.DataSourceManager;
import com.exercise.dto.FruitDto;

public class FruitDao {

    public List<FruitDto> findAll() throws SQLException, NamingException {
        String sql = "SELECT * FROM FRUIT";
        List<FruitDto> fruitList = new ArrayList<>();
        try (Connection con = DataSourceManager.getConnection();
                PreparedStatement ps = con.prepareStatement(sql)) {
            ResultSet rs = ps.executeQuery();
            while (rs.next()) {
                FruitDto fruit = new FruitDto();
                fruit.setName(rs.getString("NAME"));
                fruit.setOrigin(rs.getString("ORIGIN"));
                fruit.setPrice(rs.getInt("PRICE"));
                fruitList.add(fruit);
            }
        }
        return fruitList;
    }

    // TODO（追加処理）
}
```

**BookDto.java（パッケージ：com.exercise.dto）**

```java
package com.exercise.dto;

public class BookDto {

    private int id;
    private String title;
    private int price;

    public int getId() {
        return id;
    }
    public void setId(int id) {
        this.id = id;
    }
    public String getTitle() {
        return title;
    }
    public void setTitle(String title) {
        this.title = title;
    }
    public int getPrice() {
        return price;
    }
    public void setPrice(int price) {
        this.price = price;
    }
}
```

**DataSourceManager.java（パッケージ：com.exercise）**

```java
package com.exercise;

import java.sql.Connection;
import java.sql.SQLException;
import javax.naming.Context;
import javax.naming.InitialContext;
import javax.naming.NamingException;
import javax.sql.DataSource;

public class DataSourceManager {
    public static Connection getConnection() throws NamingException, SQLException {
        try {
            Context context = new InitialContext();
            DataSource dataSource = (DataSource) context.lookup("java:comp/env/jdbc/example");
            return dataSource.getConnection();
        } catch (SQLException | NamingException e) {
            throw e;
        }
    }
}
```

**context.xml**　※WebContent > META-INFフォルダに配置する。

```xml
<?xml version="1.0" encoding="UTF-8"?>
<Context>
    <Resource name="jdbc/example" auth="Container"
        type="javax.sql.DataSource" driverClassName="com.mysql.cj.jdbc.Driver"
        url="jdbc:mysql://localhost:3306/example?useSSL=false&amp;serverTimezone=JST"
        username="root" password="mysql" maxTotal="30" maxIdle="10"
        maxWaitMillis="5000" />
</Context>
```

**DDL**

```
DROP TABLE IF EXISTS FRUIT;

CREATE TABLE FRUIT (
    ID INTEGER PRIMARY KEY AUTO_INCREMENT,
    NAME VARCHAR(100),
    ORIGIN VARCHAR(50),
    PRICE INTEGER
);

INSERT INTO FRUIT (NAME, ORIGIN, PRICE) VALUES ('Apple', '青森県', 200);
INSERT INTO FRUIT (NAME, ORIGIN, PRICE) VALUES ('Banana', 'フィリピン', 100);
INSERT INTO FRUIT (NAME, ORIGIN, PRICE) VALUES ('Cherry', '山形県', 500);
```

**jquery8.jsp**

```html
<%@page import="com.exercise.dto.FruitDto"%>
<%@page import="java.util.List"%>
<%@page import="com.exercise.dao.FruitDao"%>
<%@ page language="java" contentType="text/html; charset=UTF-8"
    pageEncoding="UTF-8"%>
<%@ taglib uri="http://java.sun.com/jsp/jstl/core" prefix="c"%>
<%
    FruitDao dao = new FruitDao();
    List<FruitDto> fruitList = dao.findAll();
    request.setAttribute("fruitList", fruitList);
%>
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>jQuery演習</title>
<script src="https://code.jquery.com/jquery-3.3.1.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.7/umd/popper.min.js"></script>
<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.2.1/css/bootstrap.min.css">
<script type="text/javascript">
$(function() {
    // TODO
});
</script>
</head>
<body>
    <div class="container">
        <div class="row">
            <div class="col-8">
                <h1>フルーツ一覧</h1>
                <div id="message"></div>
                <table id="fruits-list" class="table table-hover">
                    <tr>
                        <th>商品名</th>
                        <th>産地</th>
                        <th>価格</th>
                    </tr>
                    <c:forEach var="fruit" items="${fruitList}">
                        <tr>
                            <td><c:out value="${fruit.name}" /></td>
                            <td><c:out value="${fruit.origin}" /></td>
                            <td><c:out value="${fruit.price}" />円</td>
                        </tr>
                    </c:forEach>
                </table>
                <br>
                フルーツ名：<input type="text" id="name" class="form-control w-50">
                産地：<input type="text" id="origin" class="form-control w-50">
                価格：<input type="number" id="price" class="form-control w-50"><br>
                <button id="add-fruit" class="btn btn-primary">追加</button>
            </div>
        </div>
    </div>
</body>
</html>
```

<br>
<hr>
