---
title: Beispiel für einen Adressbuchanbieter
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2ccf1643-5604-4fee-92cc-3d6af00e7f98
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: fa2a447d0757e75c95d7dc3d9b1dd16b8c7a8084
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331108"
---
# <a name="address-book-provider-sample"></a>Beispiel für einen Adressbuchanbieter

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
In diesem Beispiel wird ein einzelner schreibgeschützter Container für Anzeigenamen und e-Mail-Adressen unterstützt, die aus einer Flatfile-Binärdatei gelesen werden. Das Beispiel unterstützt einmalige Vorlagen und alle Konfigurationsoptionen mit Ausnahme des Profil-Assistenten.
  
Sie können dieses Beispiel aus [MAPI-Code Beispielen (Outlook Messaging API)](https://go.microsoft.com/fwlink/?LinkId=129740
)herunterladen.
  
|||
|:-----|:-----|
|Executable  <br/> |SABP32. dll  <br/> |
| Quellcodeverzeichnis:  <br/> |SampleAddressBookProvider\SABP  <br/> |
|Sprache  <br/> |C++  <br/> |
|Plattformen  <br/> |Microsoft Visual Studio 2008 für die Kompilierung für Windows Vista, Windows Server 2008, Windows XP SP2 und Windows Server 2003 SP1  <br/> |
   
## <a name="supported-features"></a>Unterstützte Features

In diesem Beispiel werden die folgenden Features unterstützt:
  
- Tabellen Einschränkungen. Im Beispiel wird die Auflösung von Präfixen und mehrdeutigen Namen implementiert. Die vollständige MAPI-Einschränkungs Sprache wird nicht implementiert, und Einschränkungen werden nur für den Anzeigenamen unterstützt.
    
- Eine Details-Anzeigetabelle für Messagingbenutzer. 
    
- Einmalige Adressen.
    
- Dialogfeld Erweiterte Suche.
    
- Eine [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) -Schnittstelle. Diese Schnittstelle wird teilweise unterstützt; die **IMAPIProp** -Methoden werden an die **IPropData** -Schnittstelle delegiert. Weitere Informationen finden Sie unter der [IPropData: IMAPIProp](ipropdataimapiprop.md) -Schnittstelle. 
    
- Interaktive und programmgesteuerte Konfiguration.
    
## <a name="unsupported-features"></a>Nicht unterstützte Features

In diesem Beispiel werden die folgenden Features nicht unterstützt:
  
- Sortierung.
    
- Verteilerlisten.
    
- Erstellen, löschen und Ändern von Einträgen.
    
- Eigenschaften mit mehreren Werten.
    
- Benannte Eigenschaften.
    
- Unterscheidung zwischen vor-und Nachnamen in Anzeigenamen.
    
 **So installieren Sie den Beispiel-Adressbuchanbieter**
  
1. Informationen zum Herunterladen des Beispiel-Adressbuch Anbieters finden Sie unter [herunterladen der Outlook-MAPI-Beispiele](downloading-the-outlook-mapi-samples.md).
    
2. Suchen Sie den Ordner, in dem Sie die Outlook-MAPI-Beispiele gespeichert haben. Klicken Sie mit der rechten Maustaste auf den Zip **-Ordner OutlookMAPISamples-\<Versions\> Nummer** , und klicken Sie auf **Alle extrahieren**.
    
3. Klicken Sie auf **Durchsuchen**, wählen Sie den Speicherort aus, an dem Sie das Beispiel speichern möchten, und klicken Sie auf **extrahieren**.
    
4. Führen Sie Visual Studio 2008 aus.
    
5. Klicken Sie in Visual Studio 2008 auf **Datei**, wählen Sie **Öffnen**aus, und klicken Sie dann auf **Projekt/Lösung**.
    
6. Navigieren Sie zu dem Speicherort, an dem Sie das Beispiel gespeichert haben, klicken Sie auf **SABP. vcproj**, und klicken Sie dann auf **Öffnen**.
    
7. On the **Build** menu, click **Build Solution**.
    
8. Klicken Sie im Dialogfeld **Datei speichern** unter auf **Speichern**.
    
9. Klicken Sie in dem Ordner, in dem Sie das Beispiel gespeichert haben, mit der rechten Maustaste auf die Datei **install. bat** , und klicken Sie dann auf **als Administrator ausführen**.
    
10. Klicken Sie im Dialogfeld **Benutzerkontensteuerung** auf **Weiter**.
    
    > [!NOTE]
    > **Install. bat** kopiert die dll in den standardMäßigen Microsoft Office-Installationsordner, c:\Programme\Microsoft Office\Office12\. Wenn Sie Office-Produkte an einem anderen Speicherort installiert haben, klicken Sie mit der rechten Maustaste auf **install. bat** , und klicken Sie auf **Bearbeiten**. Die Datei wird im Editor geöffnet. Ersetzen Sie den Standardinstallationspfad durch den Installationspfad, der auf Ihrem Computer verwendet wird. 
  

