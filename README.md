# 🏨 Hotellstyringssystem 
Et hotelladministrasjonssystem utviklet i .NET, Blazor og MAUI. Systemet håndterer rombooking, kundeadministrasjon og rengjøringsstatus.

## 🚀 Applikasjoner
Prosjektet består av flere applikasjoner:

### **🖥️ DesktopApp for Front Desk**
- Lages med **WPF**.
- Bruker **DatabaseLibrary** for å hente data fra databasen.
- Håndterer innsjekk og utsjekk.

### **🌍 WebApp for Booking**
- Lages med **Blazor**.
- Lar kunder søke etter og bestille rom.
- Bruker **DatabaseLibrary** for å hente data.

### **📱 App for Cleaning Personell**
- Lages med **.NET MAUI**.
- Viser rengjøringspersonell hvilke rom som trenger vedlikehold.
- Oppdaterer rengjøringsstatus i databasen.

### **🗄️ DatabaseLibrary**
- Inneholder klasser for databasekommunikasjon.
- Bruker **Entity Framework Core** og scaffolding for å generere modellklasser.

---

## 📊 Database
Systemet bruker følgende databasetabeller:

### **🛏️ Romdata**
| id  | kvalitet  | antall_senger |
|----|----------|--------------|
| PK  | String   | Integer      |

### **📅 Bookingdata**
| id  | rom_id (FK) | startdato | sluttdato | antall_personer |
|----|------------|----------|----------|----------------|
| PK  | FK til Romdata | Date | Date | Integer |

### **💰 Prisdata**
| kvalitet (PK, FK) | pris |
|------------------|------|
| String | Float |

### **👤 Kunde-brukere**
| id  | navn | telefon | epost | passord_hash | passord_salt |
|----|------|--------|------|--------------|-------------|
| PK  | String | String | String | Hashed String | Salted String |
