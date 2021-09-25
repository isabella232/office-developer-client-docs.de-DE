---
title: Adressbuchanbieterbeispiel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 2ccf1643-5604-4fee-92cc-3d6af00e7f98
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 66477d096dae5c9243a251d4c592856297d4456d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580293"
---
# <a name="address-book-provider-sample"></a>Adressbuchanbieterbeispiel

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
In diesem Beispiel wird ein einzelner schreibgeschützter Container für Anzeigenamen und E-Mail-Adressen unterstützt, die aus einer flachen Binärdatei gelesen werden. Das Beispiel unterstützt einmalige Vorlagen und alle Konfigurationsoptionen mit Ausnahme des Profil-Assistenten.
  
Sie können dieses Beispiel aus [Outlook MapI-Codebeispielen (Messaging API)](https://go.microsoft.com/fwlink/?LinkId=129740
)herunterladen.
  
|||
|:-----|:-----|
|Ausführbaren:  <br/> |SABP32.dll  <br/> |
| Quellcodeverzeichnis:  <br/> |SampleAddressBookProvider\SABP  <br/> |
|Sprache:  <br/> |C++  <br/> |
|Plattformen:  <br/> |Microsoft Visual Studio 2008 zum Kompilieren für Windows Vista, Windows Server 2008, Windows XP SP2 und Windows Server 2003 SP1  <br/> |
   
## <a name="supported-features"></a>Unterstützte Features

In diesem Beispiel werden die folgenden Features unterstützt:
  
- Tabelleneinschränkungen. Im Beispiel werden präfixübereinstimmung und mehrdeutige Namensauflösung implementiert. Es implementiert nicht die vollständige MAPI-Einschränkungssprache, und Einschränkungen werden nur für den Anzeigenamen unterstützt.
    
- Eine Detailanzeigetabelle für Messagingbenutzer. 
    
- Einmalige Adressen.
    
- Ein Dialogfeld für die erweiterte Suche.
    
- Eine [IMAPIStatus : IMAPIProp-Schnittstelle.](imapistatusimapiprop.md) Diese Schnittstelle wird teilweise unterstützt. Die **IMAPIProp-Methoden** werden an die **IPropData-Schnittstelle** delegiert. Weitere Informationen finden Sie unter der [IPropData : IMAPIProp-Schnittstelle.](ipropdataimapiprop.md) 
    
- Interaktive und programmgesteuerte Konfiguration.
    
## <a name="unsupported-features"></a>Nicht unterstützte Features

In diesem Beispiel werden die folgenden Features nicht unterstützt:
  
- Sortieren.
    
- Verteilerlisten.
    
- Erstellen, Löschen und Ändern von Einträgen.
    
- Eigenschaften mit mehreren Werten.
    
- Benannte Eigenschaften.
    
- Unterscheidung zwischen Vor- und Nachnamen in Anzeigenamen.
    
 **So installieren Sie den Beispieladressbuchanbieter**
  
1. Informationen zum Herunterladen des Beispieladressbuchanbieters finden Sie unter [Herunterladen der Outlook MAPI-Beispiele.](downloading-the-outlook-mapi-samples.md)
    
2. Suchen Sie den Ordner, in dem Sie die Outlook MAPI-Beispiele gespeichert haben. Klicken Sie mit der rechten Maustaste auf den Ordner **"OutlookMAPISamples- \<version number\>** zip", und klicken Sie auf **"Alle extrahieren".**
    
3. Klicken Sie auf **Durchsuchen,** wählen Sie den Speicherort aus, an dem Sie das Beispiel speichern möchten, und klicken Sie auf **"Extrahieren".**
    
4. Führen Sie Visual Studio 2008 aus.
    
5. Klicken Sie in Visual Studio 2008 auf **"Datei",** wählen Sie **"Öffnen"** aus, und klicken Sie dann auf **Project/Lösung.**
    
6. Navigieren Sie zu dem Speicherort, an dem Sie das Beispiel gespeichert haben, klicken Sie auf **"SABP.vcproj"** und dann auf **"Öffnen".**
    
7. On the **Build** menu, click **Build Solution**.
    
8. Klicken Sie im Dialogfeld **"Datei speichern unter"** auf **"Speichern".**
    
9. Klicken Sie in dem Ordner, in dem Sie das Beispiel gespeichert haben, mit der rechten Maustaste auf die **dateiinstall.bat,** und klicken Sie auf **"Als Administrator ausführen".**
    
10. Klicken Sie im Dialogfeld **Benutzerkontensteuerung** auf **Weiter**.
    
    > [!NOTE]
    > **Install.bat** kopiert die .dll in den Standardinstallationsordner Microsoft Office C:\Programme\Microsoft Office\Office12.\. Wenn Sie Office Produkte an einem anderen Speicherort installiert haben, klicken Sie mit der rechten Maustaste auf **Install.bat,** und klicken Sie auf **"Bearbeiten".** Die Datei wird in Editor geöffnet. Ersetzen Sie den Standardinstallationspfad durch den installationspfad, der auf Ihrem Computer verwendet wird. 
  

