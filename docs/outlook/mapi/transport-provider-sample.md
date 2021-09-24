---
title: Transportanbieterbeispiel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: ec6eb6c0-bfe3-4989-9071-89a14c0e7bdd
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e40bb5049c20923de1ba9cce9cf05e3e90f4aa34
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59549855"
---
# <a name="transport-provider-sample"></a>Transportanbieterbeispiel

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
In diesem Beispiel werden Dateien und Verzeichnisse zum Übertragen und Empfangen von Nachrichten verwendet. Es implementiert und registriert einen sehr einfachen Präprozessor, der eine Textzeile an jede ausgehende Nachricht anfügt. Das Beispiel veranschaulicht, wie Nachrichteninhalte zwischen transportneutralem Kapselungsformat (Transport Neutral Encapsulation Format, TNEF) und Text aufgeteilt werden. Außerdem werden alle Konfigurationsoptionen (Eigenschaftenblätter, Assistenten und programmgesteuerte Konfiguration) und Nachrichtenoptionen unterstützt. Die Remote-Transportschnittstellen werden nicht unterstützt. 
  
Sie können dieses Beispiel aus [Outlook MapI-Codebeispielen (Messaging API)](https://go.microsoft.com/fwlink/?LinkId=129740)herunterladen.
  
|||
|:-----|:-----|
|Ausführbaren:  <br/> |mrxp32.dll  <br/> |
|Quellcodeverzeichnis:  <br/> |SampleTransportProvider\MRXP  <br/> |
|Sprache:  <br/> |C++  <br/> |
|Plattformen:  <br/> |Visual Studio 2008 zum Kompilieren für Windows Vista, Windows Server 2008, Windows XP SP2 und Windows Server 2003 SP1  <br/> |
   
## <a name="supported-features"></a>Unterstützte Features

In diesem Beispiel werden die folgenden Features unterstützt:
  
- Grundlegende Features wie das Senden, Empfangen und Abfragen neuer Nachrichten.
    
- Interaktive und programmgesteuerte Konfiguration.
    
- Die **IMAPIStatus-Schnittstelle,** mit Ausnahme der Eigenschaftseinstellung. Weitere Informationen finden Sie unter der [IMAPIStatus : IMAPIProp-Schnittstelle.](imapistatusimapiprop.md) 
    
- Threadsicherheit.
    
- Ereignisprotokollierung in einer Textdatei. Die Datei wird automatisch auf eine angegebene Größe beschränkt. Alle Transportsitzungen verwenden dieselbe Datei.
    
## <a name="unsupported-features"></a>Nicht unterstützte Features

In diesem Beispiel wird die asynchrone Erkennung eingehender Nachrichten nicht unterstützt.
  
 **So installieren Sie den Beispieltransportanbieter**
  
1. Informationen zum Herunterladen des Beispiel-Transportanbieters finden Sie unter [Herunterladen der Outlook MAPI-Beispiele.](downloading-the-outlook-mapi-samples.md)
    
2. Suchen Sie den Ordner, in dem Sie die Outlook MAPI-Beispiele gespeichert haben. Klicken Sie mit der rechten Maustaste auf den Ordner **"OutlookMAPISamples- \<version number\>** zip", und klicken Sie auf **"Alle extrahieren".**
    
3. Klicken Sie auf **Durchsuchen,** wählen Sie den Speicherort aus, an dem Sie das Beispiel speichern möchten, und klicken Sie auf **"Extrahieren".**
    
4. Führen Sie Visual Studio 2008 aus.
    
5. Klicken Sie in Visual Studio 2008 auf **"Datei",** wählen Sie **"Öffnen"** aus, und klicken Sie dann auf **Project/Lösung.**
    
6. Navigieren Sie zu dem Speicherort, an dem Sie das Beispiel gespeichert haben, klicken Sie auf **"mrxp32.vcproj",** und klicken Sie dann auf **"Öffnen".**
    
7. Klicken Sie im Menü **"Erstellen"** auf **"Configuration Manager".**
    
8. Wechseln Sie im Dialogfeld **Configuration Manager** zur Zeile **"mrxp32",** wählen Sie in der Spalte **"Konfiguration"** die Option **"Freigeben"** aus, und klicken Sie dann auf **"Schließen".**
    
9. On the **Build** menu, click **Build Solution**.
    
10. Klicken Sie im Dialogfeld **"Datei speichern unter"** auf **"Speichern".**
    
11. Klicken Sie in dem Ordner, in dem Sie das Beispiel gespeichert haben, mit der rechten Maustaste auf die Installationsbatchdatei, und klicken Sie auf **"Als Administrator ausführen".**
    
12. Klicken Sie im Dialogfeld **Benutzerkontensteuerung** auf **Weiter**.
    
    > [!NOTE]
    > **install.bat** kopiert die .dll in den Standardinstallationsordner Microsoft Office C:\Programme\Microsoft Office\Office12.\. Wenn Sie Office Produkte an einem anderen Speicherort installiert haben, klicken Sie mit der rechten Maustaste auf **install.bat,** und klicken Sie auf **"Bearbeiten".** Die Datei wird in Editor geöffnet. Ersetzen Sie den Standardinstallationspfad durch den installationspfad, der auf Ihrem Computer verwendet wird. 
  
 **So richten Sie den Transportanbieter in Outlook**
  
1. Klicken  Sie im Menü Extras von Outlook auf **Konto Einstellungen.**
    
2. Klicken Sie im Dialogfeld **Konto Einstellungen** auf der Registerkarte E-Mail auf **Neu.** 
    
3. Klicken Sie unter **"E-Mail-Dienst auswählen"** auf **"Andere",** wählen Sie **"MRXP-Beispieltransport"** aus, und klicken Sie dann auf **"Weiter".**
    
4. Geben Sie im Dialogfeld **MRXP-Transportkonfiguration** einen **Benutzeranzeigenamen** ein.
    
5. Geben Sie unter **"Pfad zum Posteingang" (UNC-Freigabe)** einen Ordnerpfad ein. Dies kann auch ein Pfad zu einem lokalen Ordner sein. 
    
    > [!IMPORTANT]
    > Dieser Pfad muss vorhanden sein. 
  
6. Klicken Sie auf **OK**.
    
7. Klicken Sie im Dialogfeld **E-Mail-Konto hinzufügen** auf **OK.** Klicken Sie auf **Fertig stellen** und dann auf **"Schließen".**
    
8. Um mit der Verwendung des MRXP-Kontos zu beginnen, beenden Sie Outlook, und starten Sie es neu.
    
 **So verwenden Sie das Transportanbieterbeispiel zum Senden einer Nachricht in Outlook**
  
1. Klicken Sie im Menü **"Datei"** auf **"Neu"** und dann auf **"E-Mail-Nachricht".**
    
2. Geben Sie im Feld **"An"** den Namen des Empfängers im Format **[MRXP: \<ADDRESS\> ]** ein. Die Adresse ist die UNC-Freigabe oder der lokale Ordnerpfad zum Posteingang des Empfängers.
    
    > [!NOTE]
    > Wenn die Adresse Doppelpunkte oder umgekehrte Schrägstriche enthält, müssen Sie vor jedem Doppelpunkt oder umgekehrten Schrägstrich einen umgekehrten Schrägstrich einfügen. Um beispielsweise E-Mails an [MRXP:C:\Mail\myDir] zu senden, müssen Sie  `[MRXP:C\:\\Mail\\myDir]` . 
  
    > [!IMPORTANT]
    > Die Empfängeradresse muss vorhanden sein. 
  
3. Klicken Sie auf **"Konto"** und dann auf **"MRXP-Beispieltransport".**
    
4. Geben Sie Ihre Nachricht ein, und klicken Sie auf **"Senden".** Die Nachricht wird mithilfe des MRXP-Transportanbieters gesendet.
    
 **So verwenden Sie das Transportanbieterbeispiel zum Empfangen einer Nachricht in Outlook**
  
1. Klicken Sie im Menü **"Datei"** auf **"Neu"** und dann auf **"E-Mail-Nachricht".**
    
2. Geben Sie Ihre Nachricht ein.
    
3. Klicken Sie auf die **Schaltfläche Microsoft Office,** klicken Sie auf **"Speichern unter",** und klicken Sie dann auf **"Speichern unter",** um die Datei im Posteingangsordner zu speichern, den Sie während des Setups angegeben haben. 
    
4. Navigieren Sie im Dialogfeld **"Speichern unter"** zur UNC-Freigabe oder zum lokalen Ordner, den Sie als Posteingang festgelegt haben. 
    
5. Klicken Sie in der Dropdownliste **"Als Typ speichern"** auf **Outlook Nachrichtenformat.**
    
6. Geben Sie einen Namen für die Datei ein, und klicken Sie auf **"Speichern".**
    
7. Die Datei wird im freigegebenen Ordner gespeichert. Der MRXP-Transportanbieter übermittelt die Nachricht in Outlook an Ihren Posteingang.
    

