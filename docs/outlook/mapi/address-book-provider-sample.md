---
title: Adressbuchanbieter-Beispiel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2ccf1643-5604-4fee-92cc-3d6af00e7f98
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: fa2a447d0757e75c95d7dc3d9b1dd16b8c7a8084
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331108"
---
# <a name="address-book-provider-sample"></a>Adressbuchanbieter-Beispiel

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Dieses Beispiel unterstützt einen einzelnen schreibgeschützten Container für Anzeigenamen und E-Mail-Adressen, die aus einer Flatfile-Binärdatei ausgelesen werden. Das Beispiel unterstützt einmalige Vorlagen und alle Konfigurationsoptionen außer den Profil-Assistenten.
  
Sie können dieses Beispiel aus [Outlook-MAPI-Code-Beispiele (Messaging-API)](https://go.microsoft.com/fwlink/?LinkId=129740
) herunterladen.
  
|||
|:-----|:-----|
|Ausführbar:  <br/> |SABP32.dll  <br/> |
| Quellcode-Verzeichnis:  <br/> |SampleAddressBookProvider\SABP  <br/> |
|Sprache:  <br/> |C++  <br/> |
|Plattformen:  <br/> |Microsoft Visual Studio 2008 zum Kompilieren für Windows Vista, Windows Server 2008, Windows XP SP2 und Windows Server 2003 SP1  <br/> |
   
## <a name="supported-features"></a>Unterstützte Features

In diesem Beispiel werden die folgenden Features unterstützt:
  
- Tabelleneinschränkungen. Im Beispiel wird eine Auflösung von Namen mit Präfixübereinstimmung und mehrdeutigen Namen implementiert. Es wird nicht die vollständige MAPI-Einschränkungssprache implementiert und Einschränkungen werden nur im Anzeigenamen unterstützt.
    
- Eine Detail-Anzeigetabelle für Nachrichtenbenutzer. 
    
- Einmaladressen.
    
- Ein Dialogfeld für die erweiterte Suche.
    
- Eine [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)-Schnittstelle. Diese Schnittstelle wird teilweise unterstützt; ihre **IMAPIProp**-Methoden werden an die **IPropData**-Schnittstelle delegiert. Weitere Informationen finden Sie unter der [IPropData : IMAPIProp](ipropdataimapiprop.md)-Schnittstelle. 
    
- Interaktive und programmgesteuerte Konfiguration.
    
## <a name="unsupported-features"></a>Nicht unterstützte Features

In diesem Beispiel werden die folgenden Features nicht unterstützt:
  
- Sortieren.
    
- Verteilerlisten.
    
- Erstellen, Löschen und Ändern von Einträgen.
    
- Eigenschaften mit mehreren Werten.
    
- Benannte Eigenschaften.
    
- Unterscheidung zwischen Vor- und Nachnamen in Anzeigenamen.
    
 **So laden Sie das Beispiel für einen Adressbuchanbieter herunter**
  
1. Informationen zum Herunterladen des Beispiels für einen Adressbuchanbieter finden Sie unter [Herunterladen der Outlook-MAPI-Beispiele](downloading-the-outlook-mapi-samples.md).
    
2. Suchen Sie den Ordner, in dem die Outlook-MAPI-Beispiele gespeichert sind. Klicken Sie mit der rechten Maustaste auf den ZIP-Ordner **OutlookMAPISamples-\<Versionsnummer\>**, und klicken Sie auf **Alle extrahieren**.
    
3. Klicken Sie auf **Durchsuchen**, wählen Sie den Speicherort aus, wo Sie das Beispiel speichern wollen und klicken Sie auf **Extrahieren**.
    
4. Führen Sie Visual Studio 2008 aus.
    
5. Klicken Sie in Visual Studio 2008 auf **Datei**, wählen Sie **Öffnen** aus, und klicken Sie dann auf **Projekt/Lösung**.
    
6. Navigieren Sie zu dem Speicherort, wo Sie das Beispiel gespeichert haben, klicken Sie auf **SABP.vcproj**, und klicken Sie dann auf **Öffnen**.
    
7. Klicken Sie im Menü **Erstellen** auf **Projektmappe erstellen**.
    
8. Klicken Sie im Dialogfeld **Speichern unter** auf **Speichern**.
    
9. Klicken Sie in dem Ordner, wo Sie das Beispiel gespeichert haben, mit der rechten Maustaste auf die Datei **install.bat**, und klicken Sie auf **Als Administrator ausführen**.
    
10. Klicken Sie im Dialogfeld **Benutzerkontensteuerung** auf **Weiter**.
    
    > [!NOTE]
    > **Install.bat** kopiert die .dll in den Microsoft Office-Standardinstallationsordner, C:\Program Files\Microsoft Office\Office12\. Wenn Sie Office-Produkte an einem anderen Speicherort installiert haben, klicken Sie mit der rechten Maustaste auf **Install.bat** und klicken Sie auf **Bearbeiten**. Die Datei wird im Editor geöffnet. Ersetzen Sie den Standardinstallationspfad durch den auf dem Computer verwendeten Installationspfad. 
  

