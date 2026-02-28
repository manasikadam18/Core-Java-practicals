abstract class Patient
{
    protected String name;
    protected int age;
    protected String contact;
    private String aadhaarNumber; 
    private String insuranceId; 
    
    public Patient(String name, int age, String contact, String aadhaarNumber, String insuranceId) 
    { 
        this.name = name; 
        this.age = age; 
        this.contact = contact; 
        this.aadhaarNumber = aadhaarNumber; 
        this.insuranceId = insuranceId; 
    } 
    
    public void getDetails() 
    { 
        System.out.println("Name: " + name); 
        System.out.println("Age: " + age); 
        System.out.println("Contact: " + contact); 
    } 
    
    abstract void recordTreatment(); 
    abstract double calculateBill(); 
} 

class InPatient extends Patient 
{ 
    private String admissionDate; 
    private String roomNumber; 
    private String doctorAssigned; 
    
    public InPatient(String name, int age, String contact, String aadhaarNumber, String insuranceId, String admissionDate, String roomNumber, String doctorAssigned) 
    { 
        super(name, age, contact, aadhaarNumber, insuranceId); 
        this.admissionDate = admissionDate; 
        this.roomNumber = roomNumber; 
        this.doctorAssigned = doctorAssigned; 
    } 
    
    @Override void recordTreatment() 
    { 
        System.out.println("InPatient treatment recorded. Doctor: " + doctorAssigned); 
    } 
    
    @Override double calculateBill() 
    { 
        return 5000; 
    } 
    
    void assignRoom() 
    { 
        System.out.println("Room Assigned: " + roomNumber); 
    } 
} 

class OutPatient extends Patient 
{ 
    private String visitDate; 
    private String consultancy;
    
    public OutPatient(String name, int age, String contact, String aadhaarNumber, String insuranceId, String visitDate, String consultancy) 
    { 
        super(name, age, contact, aadhaarNumber, insuranceId); 
        this.visitDate = visitDate; 
        this.consultancy = consultancy; 
    } 
    
    @Override void recordTreatment() 
    { 
        System.out.println("OutPatient treatment recorded for consultancy: " + consultancy); 
    } 
    
    @Override double calculateBill() 
    { 
        return 800; 
    } 
    
    void arrangeAppointment() 
    { 
        System.out.println("Appointment arranged on " + visitDate); 
    } 
} 

class EmergencyPatient extends Patient 
{ 
    private String emergencyLevel; 
    private String arrivalTime; 
    private String triageCategory; 
    
    public EmergencyPatient(String name, int age, String contact, String aadhaarNumber, String insuranceId, String emergencyLevel, String arrivalTime, String triageCategory) 
    { 
        super(name, age, contact, aadhaarNumber, insuranceId); 
        this.emergencyLevel = emergencyLevel; 
        this.arrivalTime = arrivalTime; 
        this.triageCategory = triageCategory; 
    } 
    
    @Override void recordTreatment() 
    { 
        System.out.println("Emergency treatment recorded. Level: " + emergencyLevel); 
    } 
    
    @Override double calculateBill() 
    { 
        return 3000; 
    } 
    
    void prioritizeTreatment() 
    { 
        System.out.println("Triage Category: " + triageCategory + " | Arrival Time: " + arrivalTime); 
    } 
}

public class HospitalSystem 
{ 
    public static void main(String[] args) 
    { 
        Patient p1 = new InPatient("Ravi", 45, "9876543210", "1234-5678-9012", "INS001", "02-02-2026", "A101", "Dr. Mehta"); 
        Patient p2 = new OutPatient("Sneha", 30, "9123456780", "2345-6789-0123", "INS002", "03-02-2026", "Dermatology"); 
        Patient p3 = new EmergencyPatient("Arjun", 28, "9988776655", "3456-7890-1234", "INS003", "High", "10:30 AM", "Critical"); 
        System.out.println("\n--- InPatient ---"); 
        p1.getDetails(); 
        p1.recordTreatment();
        System.out.println("Bill: RS." + p1.calculateBill()); 
        System.out.println("\n--- OutPatient ---"); 
        p2.getDetails(); 
        p2.recordTreatment(); 
        System.out.println("Bill: RS." + p2.calculateBill()); 
        System.out.println("\n--- EmergencyPatient ---"); 
        p3.getDetails(); p3.recordTreatment(); 
        System.out.println("Bill: RS." + p3.calculateBill()); 
    } 
}
