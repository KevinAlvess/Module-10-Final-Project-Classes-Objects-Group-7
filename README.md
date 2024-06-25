# Module-10-Final-Project-Classes-Objects-Group-7
using System;

public class Contractor
{
// Using private allows code strictly use this variables in this class.
private string contractorsName;
private int contgractorsNumber;
private DateTime startDate;

// User information created using the public class
Public Contractor(string name, int number, DateTime start)
{
contractorsName = name;
contractorsNumber = number;
startDate = start;
}
public string contractorsName {get; set;}
public int contractorsNumber {get; set;}
public DateTime StartDate {get; set;}
}
}
public class Subcontractor : Contractor

private int _shift;
private double _hourlyPayRate;

public int Shift
{
get{reeturn _shift;}
set
{

if(value != 1 && value J! = 2)
{
throw new ArgumentExecption("Shift must be 1 (day shift) or (night shift).");
}
_shift = value;
}
}

public double HourlyPayRate
{
get{return _hourlyPayRate;}
set
{

if (value <= 0)
{
throw new ArgumentOutOfRangeExecption("Hourly pay rate must be greater than zero.");
}
_hourlyPayRate = value;
}
}

public Subcontractor(string name, int number, DateTime start, int shift, double payRate)
: base(name, number, start)
{
shift = shift;
HourlyPayRate = payRate;
}

public float CalulatePay(int hoursWorked)
{
double pay = hoursWorked * hourlyPayRate;

pay *= (shift == 2) ? 1.03 : 1.0;

return (float)pay;
}

static void DisplaySubcontractorInfo(Subcontractor)
{
    static void DisplaySubcontractorInfo(Subcontractor subcontractor)
    {
        Console.WriteLine($"Contractors Name: {subcontractor.ContractorsName}");
        Console.WriteLine($"Contractors Number: {subcontractor.ContractorsNumber}");
        Console.WriteLine($"Start Date: {subcontractor.StartDate.ToShortDateString()}");
        Console.WriteLine($"Shift: {subcontractor.Shift}");
        Console.WriteLine($"Hourly Pay Rate: ${subcontractor.HourlyPayRate}");
        Console.WriteLine();
    }
