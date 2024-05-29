# Spring_project
Медична Картотека

### Функціональні Вимоги

#### Пацієнти (Patients)

**Реєстрація Пацієнта**
Користувач повинен мати можливість зареєструвати нового пацієнта. Система повинна приймати наступні дані: ім'я, прізвище, вік, стать, адреса, контактний номер телефону. Після успішної реєстрації система повинна повертати повідомлення про успішну реєстрацію та ідентифікатор пацієнта.

**Отримання інформації про пацієнта**
Користувач повинен мати можливість отримати інформацію про конкретного пацієнта за його ідентифікатором. Система повинна повертати наступні дані: ідентифікатор пацієнта, ім'я, прізвище, вік, стать, адреса, контактний номер телефону.

#### Лікарі (Doctors)

**Реєстрація Лікаря**
Користувач повинен мати можливість зареєструвати нового лікаря. Система повинна приймати наступні дані: номер ліцензії, ім'я, прізвище, спеціалізація, контактний номер телефону. Після успішної реєстрації система повинна повертати повідомлення про успішну реєстрацію та ідентифікатор лікаря.

**Отримання інформації про лікаря**
Користувач повинен мати можливість отримати інформацію про конкретного лікаря за його ідентифікатором. Система повинна повертати наступні дані: ідентифікатор лікаря, номер ліцензії, ім'я, прізвище, спеціалізація, контактний номер телефону.

#### Медичні Заклади (Medical Facilities)

**Додавання нового медичного закладу**
Користувач повинен мати можливість додати новий медичний заклад. Система повинна приймати наступні дані: назва закладу, місто, адреса. Після успішного додавання система повинна повертати повідомлення про успішне додавання медичного закладу та ідентифікатор закладу.

**Отримання інформації про медичний заклад**
Користувач повинен мати можливість отримати інформацію про конкретний медичний заклад за його ідентифікатором. Система повинна повертати наступні дані: ідентифікатор закладу, назва закладу, місто, адреса.

#### Медичні Процедури (Medical Procedures)

**Реєстрація Медичної Процедури**
Користувач повинен мати можливість зареєструвати нову медичну процедуру. Система повинна приймати наступні дані: назва процедури, опис, вартість. Після успішної реєстрації система повинна повертати повідомлення про успішну реєстрацію та ідентифікатор процедури.

**Отримання інформації про медичну процедуру**
Користувач повинен мати можливість отримати інформацію про конкретну медичну процедуру за її ідентифікатором. Система повинна повертати наступні дані: ідентифікатор процедури, назва процедури, опис, вартість.

#### Призначення (Appointments)

**Додавання нового призначення**
Користувач повинен мати можливість додати нове призначення. Система повинна приймати наступні дані: ідентифікатор пацієнта, ідентифікатор лікаря, ідентифікатор медичного закладу, ідентифікатор медичної процедури, дата та час призначення. Після успішного додавання система повинна повертати повідомлення про успішне додавання призначення та ідентифікатор призначення.

### REST API для управління медичною картотекою

#### Пацієнти (Patients)

**Реєстрація пацієнта (Patient Registration)**
- Метод: POST
- URL: /api/patients/register
- Вхідні дані:
  - first_name (string): Ім'я
  - last_name (string): Прізвище
  - age (integer): Вік
  - sex (string): Стать
  - address (string): Адреса
  - phone_number (string): Контактний номер телефону
- Вихідні дані:
  - message (string): Повідомлення про успішну реєстрацію
  - patient_id (integer): Ідентифікатор пацієнта

**Отримання інформації про пацієнта (Get Patient Information)**
- Метод: GET
- URL: /api/patients/{patient_id}
- Вихідні дані:
  - patient_id (integer): Ідентифікатор пацієнта
  - first_name (string): Ім'я
  - last_name (string): Прізвище
  - age (integer): Вік
  - sex (string): Стать
  - address (string): Адреса
  - phone_number (string): Контактний номер телефону

#### Лікарі (Doctors)

**Реєстрація лікаря (Doctor Registration)**
- Метод: POST
- URL: /api/doctors/register
- Вхідні дані:
  - license_number (string): Номер ліцензії
  - first_name (string): Ім'я
  - last_name (string): Прізвище
  - specialization (string): Спеціалізація
  - phone_number (string): Контактний номер телефону
- Вихідні дані:
  - message (string): Повідомлення про успішну реєстрацію
  - doctor_id (integer): Ідентифікатор лікаря

**Отримання інформації про лікаря (Get Doctor Information)**
- Метод: GET
- URL: /api/doctors/{doctor_id}
- Вихідні дані:
  - doctor_id (integer): Ідентифікатор лікаря
  - license_number (string): Номер ліцензії
  - first_name (string): Ім'я
  - last_name (string): Прізвище
  - specialization (string): Спеціалізація
  - phone_number (string): Контактний номер телефону

#### Медичні Заклади (Medical Facilities)

**Додавання нового медичного закладу (Add New Medical Facility)**
- Метод: POST
- URL: /api/medical_facilities
- Вхідні дані:
  - name (string): Назва закладу
  - city (string): Місто
  - address (string): Адреса
- Вихідні дані:
  - message (string): Повідомлення про успішне додавання медичного закладу
  - facility_id (integer): Ідентифікатор закладу

**Отримання інформації про медичний заклад (Get Medical Facility Information)**
- Метод: GET
- URL: /api/medical_facilities/{facility_id}
- Вихідні дані:
  - facility_id (integer): Ідентифікатор закладу
  - name (string): Назва закладу
  - city (string): Місто
  - address (string): Адреса

#### Медичні Процедури (Medical Procedures)

**Реєстрація медичної процедури (Procedure Registration)**
- Метод: POST
- URL: /api/procedures/register
- Вхідні дані:
  - name (string): Назва процедури
  - description (string): Опис
  - cost (number): Вартість
- Вихідні дані:
  - message (string): Повідомлення про успішну реєстрацію
  - procedure_id (integer): Ідентифікатор процедури

**Отримання інформації про медичну процедуру (Get Procedure Information)**
- Метод: GET
- URL: /api/procedures/{procedure_id}
- Вихідні дані:
  - procedure_id (integer): Ідентифікатор процедури
  - name (string): Назва процедури
  - description (string): Опис
  - cost (number): Вартість

#### Призначення (Appointments)

**Додавання нового призначення (Add New Appointment)**
- Метод: POST
- URL: /api/appointments
- Вхідні дані:
  - patient_id (integer): Ідентифікатор пацієнта
  - doctor_id (integer): Ідентифікатор лікаря
  - facility_id (integer): Ідентифікатор медичного закладу
  - procedure_id (integer): Ідентифікатор медичної процедури
  - appointment_date (string): Дата та час призначення
- Вихідні дані:
  - message (string): Повідомлення про успішне додавання

 призначення
  - appointment_id (integer): Ідентифікатор призначення

**Отримання інформації про призначення (Get Appointment Information)**
- Метод: GET
- URL: /api/appointments/{appointment_id}
- Вихідні дані:
  - appointment_id (integer): Ідентифікатор призначення
  - patient_id (integer): Ідентифікатор пацієнта
  - doctor_id (integer): Ідентифікатор лікаря
  - facility_id (integer): Ідентифікатор медичного закладу
  - procedure_id (integer): Ідентифікатор медичної процедури
  - appointment_date (string): Дата та час призначення

### Взаємозв'язки (Relationships)

**Зв'язок пацієнтів та лікарів (Patient_has_Doctor)**
- Метод: POST
- URL: /api/patient_doctors
- Вхідні дані:
  - patient_id (integer): Ідентифікатор пацієнта
  - doctor_id (integer): Ідентифікатор лікаря
- Вихідні дані:
  - message (string): Повідомлення про успішне додавання зв'язку

**Зв'язок лікарів та медичних закладів (Doctor_has_Medical_Facility)**
- Метод: POST
- URL: /api/doctor_facilities
- Вхідні дані:
  - doctor_id (integer): Ідентифікатор лікаря
  - facility_id (integer): Ідентифікатор медичного закладу
- Вихідні дані:
  - message (string): Повідомлення про успішне додавання зв'язку

**Зв'язок медичних закладів та процедур (Medical_Facility_has_Procedure)**
- Метод: POST
- URL: /api/facility_procedures
- Вхідні дані:
  - facility_id (integer): Ідентифікатор медичного закладу
  - procedure_id (integer): Ідентифікатор медичної процедури
- Вихідні дані:
  - message (string): Повідомлення про успішне додавання зв'язку

**Зв'язок пацієнтів та призначень (Patient_has_Appointment)**
- Метод: POST
- URL: /api/patient_appointments
- Вхідні дані:
  - patient_id (integer): Ідентифікатор пацієнта
  - appointment_id (integer): Ідентифікатор призначення
- Вихідні дані:
  - message (string): Повідомлення про успішне додавання зв'язку
