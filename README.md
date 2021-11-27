# javafx

//create one-screen desktop-based application in javafx

package mypack;

import javafx.application.Application;

import javafx.geometry.Pos;

import javafx.scene.Scene;

import javafx.scene.control.Button;

import javafx.scene.control.TextField;

import javafx.scene.layout.VBox;

import javafx.stage.Stage;




public class Sample extends Application {

//Application is the parent class


public static void main(String[] args) {


Application.launch(args);

//program starts with this


}@Override

public void start(Stage primaryStage) throws Exception {

//going with VBox layout

VBox pane = new VBox(); 

pane.setAlignment(Pos.CENTER);

//Two text fields 

TextField tf1 = new TextField();

TextField tf2 = new TextField();


//adding submit button

Button b = new Button("Submit");

b.setAlignment(Pos.CENTER);

//setting number of spaces in text field

tf1.setPrefColumnCount(14);

tf2.setPrefColumnCount(14);

//places all text fields on window

pane.getChildren().addAll( tf1,  tf2,b);



Scene scene = new Scene(pane, 500, 500);

primaryStage.setTitle("'INTERNSHALA' Assignment");

primaryStage.setScene(scene);

primaryStage.show();


//setting the button's action 

b.setOnAction(e->System.out.println("You entered:\nText_1:  "+tf1.getText()+""+"\nText_2: "+tf2.getText()));

}

}

![output_javafx](https://user-images.githubusercontent.com/95141207/143690632-c77c4820-799f-4fcf-a42f-3585137d2bbd.png)
