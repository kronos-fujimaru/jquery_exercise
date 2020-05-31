# jQuery 演習問題（解答例）

## 演習1

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
	$("h3").css({color:"red", backgroundColor:"yellow"});
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

## 演習2

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
	$("#sample").val("Hello jQuery!");
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

## 演習3

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
	$("#fruits").append("<li>Apple</li>");
	$("#fruits").append("<li>Banana</li>");
	$("#fruits").append("<li>Cherry</li>");
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

## 演習4

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
	$("#add-fruit").on("click", function() {
		$("#fruits-list").append("<li>" + $("#fruit").val() + "</li>");
		$("#fruit").val("");
	});
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

## 演習5

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
	$("#add-fruit").on("click",function() {
		$("#fruits-list").append("<tr></tr>");
		$("#fruits-list tr:last").append("<td>" + $("#name").val() + "</td>");
		$("#fruits-list tr:last").append("<td>" + $("#origin").val() + "</td>");
		$("#fruits-list tr:last").append("<td>" + $("#price").val() + "円</td>");

		$("#name, #origin, #price").val("");
	});
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

## 演習6

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
	$("#amazon, #google, #apple").on("click", function() {
		$("#site").attr("href", $(this).val());
		$("button").attr("class", "btn btn-light");
		$(this).attr("class", "btn btn-primary");
	});
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

## 演習7

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
	(中略)

	$("#site").click(function() {
		if ($("#site").attr("href") == "#") {
			alert("アクセスするサイトを選択してください。");
			return false;
		}
	});
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

## 演習8

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
	$("#login").on("click", function() {
		var id = $("#id").val();
		var password = $("#password").val();

		$("#message").empty();
		if (id == "user01" && password == "pass01") {
			$("#message").attr("class", "alert alert-primary");
			$("#message").text("ログインに成功しました。");
		} else {
			$("#message").attr("class", "alert alert-danger");
			$("#message").text("ログインIDまたはパスワードに誤りがあります。");
		}
	});
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

## 演習9

**FruitDao.java**
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
				fruit.setId(rs.getInt("ID"));
				fruit.setName(rs.getString("NAME"));
				fruit.setOrigin(rs.getString("ORIGIN"));
				fruit.setPrice(rs.getInt("PRICE"));
				fruitList.add(fruit);
			}
		}
		return fruitList;
	}

	public int create(FruitDto fruit) throws SQLException, NamingException {
		String sql = "INSERT INTO FRUIT (NAME, ORIGIN, PRICE) VALUES (?, ?, ?)";
        try (Connection con = DataSourceManager.getConnection();
        		PreparedStatement ps = con.prepareStatement(sql)) {
            ps.setString(1, fruit.getName());
            ps.setString(2, fruit.getOrigin());
            ps.setInt(3, fruit.getPrice());
            return ps.executeUpdate();
        }
    }
}
```

**AddFruitServlet.java**
```java
package com.exercise.controller;

import java.io.IOException;
import java.sql.SQLException;

import javax.naming.NamingException;
import javax.servlet.ServletException;
import javax.servlet.annotation.WebServlet;
import javax.servlet.http.HttpServlet;
import javax.servlet.http.HttpServletRequest;
import javax.servlet.http.HttpServletResponse;

import com.exercise.dao.FruitDao;
import com.exercise.dto.FruitDto;

/**
 * Servlet implementation class AddFruitServlet
 */
@WebServlet("/add-fruit")
public class AddFruitServlet extends HttpServlet {
	private static final long serialVersionUID = 1L;

	/**
	 * @see HttpServlet#doPost(HttpServletRequest request, HttpServletResponse response)
	 */
	protected void doPost(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {

		String name = request.getParameter("name");
		String origin = request.getParameter("origin");
		int price = Integer.parseInt(request.getParameter("price"));

        try {
        	FruitDao dao = new FruitDao();
        	FruitDto fruit = new FruitDto();

        	fruit.setName(name);
        	fruit.setOrigin(origin);
        	fruit.setPrice(price);

        	dao.create(fruit);
        } catch (SQLException | NamingException e) {
        	e.printStackTrace();
        }
	}
}
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
	$("#add-fruit").on("click", function() {
		$("#message").empty();
		$.ajax({
			type: "POST",
			url: "/jquery_sample/add-fruit",
			data: {
				"name": $("#name").val(),
				"origin": $("#origin").val(),
				"price": $("#price").val()
			}
        }).done(function() {
			$("#fruits-list").append("<tr></tr>");
			$("#fruits-list tr:last").append("<td>" + $("#name").val() + "</td>");
			$("#fruits-list tr:last").append("<td>" + $("#origin").val() + "</td>");
			$("#fruits-list tr:last").append("<td>" + $("#price").val() + "円</td>");

			$("#name, #origin, #price").val("");

			$("#message").attr("class", "alert alert-primary");
			$("#message").text("フルーツを追加しました。");
		}).fail(function() {
			$("#message").attr("class", "alert alert-danger");
			$("#message").text("フルーツの追加に失敗しました。");
		});
	});
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
