package org.firstinspires.ftc.teamcode;
//created by Nick Howard Nickynoodle16 on September 11, 2018 in OnBot Java. This is our tank drive code for team 4266 for the Rover Ruckus season.
import com.qualcomm.robotcore.eventloop.opmode.TeleOp;
import com.qualcomm.robotcore.robot.Robot;
import com.qualcomm.robotcore.eventloop.opmode.LinearOpMode;
import com.qualcomm.robotcore.eventloop.opmode.OpMode;
import com.qualcomm.robotcore.hardware.DcMotor;
import com.qualcomm.robotcore.util.ElapsedTime;

@TeleOp(name="TankDrive", group = "TankDrive")

public class TankDrive extends OpMode {
    
    //motor variables
    private ElapsedTime runtime = new ElapsedTime();
    private DcMotor leftmotor=null;
    private DcMotor rightmotor=null;
    private DcMotor leftintake=null;
    private DcMotor rightintake=null;
    //public void init is when button is pressed once
     public void init() {
        telemetry.addData("Status", "Your robot is initialized");
        telemetry.update();
        leftmotor = hardwareMap.dcMotor.get("leftmotor");
        rightmotor = hardwareMap.dcMotor.get("rightmotor");
        leftintake = hardwareMap.dcMotor.get("leftintake");
        rightintake = hardwareMap.dcMotor.get("rightintake");
        
        leftmotor.setPower(0);
        rightmotor.setPower(0);
        leftintake.setPower(0);
        rightintake.setPower(0);
    }
     public void loop(){
        //when the robot is started, you may drive it
        telemetry.update();
        double left = gamepad1.left_stick_y;
        double right = gamepad1.right_stick_y;
        boolean leftbutton = gamepad1.left_bumper;
        boolean rightbutton = gamepad1.right_bumper;
        
        leftmotor.setPower(left);
        rightmotor.setPower(right);
        //if leftbutton is pressed set power to the intake motors. If not, leave them at 0
        if (leftbutton){
            leftintake.setPower(1);
            rightintake.setPower(-1);
        }else{
            leftintake.setPower(0);
            rightintake.setPower(0);
        }
        if (rightbutton){
            leftintake.setPower(-1);
            rightintake.setPower(1);
        }else{
            leftintake.setPower(0);
            rightintake.setPower(0);
        
        } 
        telemetry.addData("Status","Run Time: "+runtime.toString());
        telemetry.addData("Motors","left(%.2f),right(%.2f)",left,right);
     //above are the commands for telemetry for the Runtime as well as motor power.
} 
     public void stop() {
        leftmotor.setPower(0);
        rightmotor.setPower(0);
        leftmotor.setPower(0);
        rightmotor.setPower(0);
        telemetry.addData("Status", "Robot is stopped.");
        telemetry.update();
     }

}
    // End of code. Nothing to see here

