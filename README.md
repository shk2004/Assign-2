# Assign-2
from enum import Enum

class DentalCompany:
    def __init__(self, name):
        self.name = name
        self.branches = []

    def add_branch(self, branch):
        self.branches.append(branch)

class Clinic:
    def __init__(self, name, address, phone_number, manager):
        self.name = name
        self.address = address
        self.phone_number = phone_number
        self.manager = manager
        self.staff = []
        self.patients = []
        self.services = []

    def add_staff(self, staff_member):
        self.staff.append(staff_member)

    def add_patient(self, patient):
        self.patients.append(patient)

    def add_service(self, service):
        self.services.append(service)

class Staff:
    def __init__(self, f_name, l_name, phone_number, emirates_id, job):
        self.f_name = f_name
        self.l_name = l_name
        self.phone_number = phone_number
        self.emirates_id = emirates_id
        self.job = job

class Manager(Staff):
    def __init__(self, f_name, l_name, phone_number, emirates_id, job, branch, salary):
        super().__init__(f_name, l_name, phone_number, emirates_id, job)
        self.branch = branch
        self.salary = salary

class Dentist(Staff):
    def __init__(self, f_name, l_name, phone_number, emirates_id, job, branch, salary):
        super().__init__(f_name, l_name, phone_number, emirates_id, job)
        self.branch = branch
        self.salary = salary

class Nurse(Staff):
    def __init__(self, f_name, l_name, phone_number, emirates_id, job, branch, salary):
        super().__init__(f_name, l_name, phone_number, emirates_id, job)
        self.branch = branch
        self.salary = salary

class PatientAppointment:
    def __init__(self, f_name, l_name, phone_number, emirates_id, time, date, year):
        self.f_name = f_name
        self.l_name = l_name
        self.phone_number = phone_number
        self.emirates_id = emirates_id
        self.time = time
        self.date = date
        self.year = year

class Patient:
    def __init__(self, f_name, l_name, phone_number, emirates_id, appointment=None, services=None):
        self.f_name = f_name
        self.l_name = l_name
        self.phone_number = phone_number
        self.emirates_id = emirates_id
        self.appointment = appointment
        self.services = services or []

class RecordTrack:
    def __init__(self, f_name, l_name, phone_number, emirates_id, appointments=None, payments=0):
        self.f_name = f_name
        self.l_name = l_name
        self.phone_number = phone_number
       
