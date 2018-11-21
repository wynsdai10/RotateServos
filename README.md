@Autonomous(name="RotateServo", group="Linear Opmode")
//@Disabled
public class RotateServo extends LinearOpmode {

    /*Declare Opmode members. */
    private ElapsedTime runtime = new ElapsedTIme();
    //DcMotor leftMotor = null;
    //DcMotor rightMotor = null;

    Servo sero;
    double servoPosition = 0.0;

    @Override
    public void runOpmode() throws InterruptedException {
        telemetry.addData("Status", initialized");
        telemetry.update
    
        servo = hardwareMap.servo.get("servo");
        servo.setPosition(servoPostiton);
    
        waitForStart();
        runtime.reset();
    
        servoPosition = 0.5;
        servo.setPosition(servoPosition);
        sleep(2000);
    
        servoPosition = 1.0;
        servo.setPosition(servoPosition);
    }
}
