package warungseblakhate;

import java.net.URL;
import java.util.ResourceBundle;
import javafx.event.ActionEvent;
import javafx.fxml.FXML;
import javafx.fxml.Initializable;
import javafx.scene.control.Button;
import javafx.scene.control.ComboBox;
import javafx.scene.control.Hyperlink;
import javafx.scene.control.Label;
import javafx.scene.control.PasswordField;
import javafx.scene.control.TextField;
import javafx.scene.layout.AnchorPane;

/**
 *
 * @author sonya
 */
public class FXMLDocumentController implements Initializable {
    
    @FXML
    private AnchorPane su_signupForm;

    @FXML
    private TextField su_username;

    @FXML
    private PasswordField su_password;

    @FXML
    private ComboBox<?> su_pertanyaan;

    @FXML
    private TextField su_jawaban;

    @FXML
    private Button su_signupBtn;

    @FXML
    private AnchorPane si_loginform;

    @FXML
    private TextField si_Username;


    @FXML
    private Button si_loginbtn;

    @FXML
    private Hyperlink si_lupapass;

    @FXML
    private AnchorPane side_form;

    @FXML
    private Button side_createBtn;
    
     @FXML
    private Button side_alreadyhave;
    
    
    public void switchForm(ActionEvent event){
        
        TranslateTransition slider = new TranslateTransition();
        if(event.getSource()== side_createBtn){
            slider.setNode(side_form);
            slider.setTox(300);
            silder.setDuration(Duration.seconds(.5));
            
            silder.setOnFinished((ActionEvent e)->{
                side_alreadyhave.setVisible(true);
                side_createBtn.setVisible(false);
            });
            
            slider.play();
        }else if (event.getSource()== side_alreadyhave){
            slider.setNode(side_form);
            slider.setTox(0);
            slider.setDuration(Duration.seconds(.5));
            
            silder.setOnFinished((ActionEvent e)->{
                side_alreadyhave.setVisible(false);
                side_createBtn.setVisible(true);
        }
        
    }
    
    @Override
    public void initialize(URL url, ResourceBundle rb) {
        // TODO
    }    
    
}
