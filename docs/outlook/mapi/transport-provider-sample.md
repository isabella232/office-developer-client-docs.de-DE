---
title: Beispiel für einen Transportanbieter
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ec6eb6c0-bfe3-4989-9071-89a14c0e7bdd
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3b3ae4170cab109ae96a51eae6e70c674895eeae
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575784"
---
# <a name="transport-provider-sample"></a>Beispiel für einen Transportanbieter

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
In diesem Beispiel werden Dateien und Verzeichnisse senden und Empfangen von Nachrichten verwendet. Es implementiert und einen sehr einfachen Präprozessor, der eine Textzeile auf jede ausgehende Nachricht anfügt registriert. Im Beispiel veranschaulicht, wie Nachrichteninhalt zwischen Transport Neutral Encapsulation Format (TNEF) und Text teilen. Außerdem werden alle Konfigurationsoptionen (Eigenschaftenseiten, Assistenten und programmgesteuerte Konfiguration) und Nachrichtenoptionen unterstützt. Es wird nicht die remote-Transport-Schnittstellen unterstützt. 
  
Sie können dieses Beispiel aus [Outlook Messaging-API (MAPI)-Codebeispiele](http://go.microsoft.com/fwlink/?LinkId=129740)herunterladen.
  
|||
|:-----|:-----|
|Ausführbare Datei:  <br/> |mrxp32.dll  <br/> |
|Code Quellverzeichnis:  <br/> |SampleTransportProvider\MRXP  <br/> |
|Sprache:  <br/> |C++  <br/> |
|Plattformen:  <br/> |Visual Studio 2008 zum Kompilieren für Windows Vista, Windows Server 2008, Windows XP SP2 und Windows Server 2003 SP1  <br/> |
   
## <a name="supported-features"></a>Unterstützte Features

In diesem Beispiel werden die folgenden Features unterstützt:
  
- Grundlegende Features wie senden, empfangen und neue Nachrichten abrufen.
    
- Interaktive und programmgesteuerte Konfiguration.
    
- Die **IMAPIStatus** -Schnittstelle, mit Ausnahme der Einstellung-Eigenschaft. Weitere Informationen finden Sie unter der [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) Schnittstelle. 
    
- Threadsicherheit.
    
- Protokollierung in eine Textdatei. Die Datei wird automatisch auf eine bestimmte Größe beschränkt. Alle Transport-Sitzungen verwenden dieselbe Datei.
    
## <a name="unsupported-features"></a>Nicht unterstützte Features

In diesem Beispiel unterstützt keine asynchronen Erkennung von eingehenden Nachrichten.
  
 **So installieren Sie den Beispielanbieter Transport**
  
1. Zum Herunterladen der Adressbuchhierarchie Beispiel finden Sie unter [Herunterladen der MAPI-Beispiele für Outlook](downloading-the-outlook-mapi-samples.md).
    
2. Suchen Sie den Ordner, in dem Sie die Outlook-MAPI-Beispiele gespeichert haben. Mit der rechten Maustaste die **OutlookMAPISamples -\<Versionsnummer\> ** zip-Ordner, und klicken Sie auf **Alle extrahieren**.
    
3. Klicken Sie auf **Durchsuchen**, markieren Sie den Speicherort, in dem Sie das Beispiel zu speichern möchten, und klicken Sie auf **extrahieren**.
    
4. Führen Sie Visual Studio 2008.
    
5. Klicken Sie in Visual Studio 2008 auf **Datei**, klicken Sie auf **Öffnen**, und klicken Sie dann auf **Projekt/Projektmappe**.
    
6. Navigieren Sie zum Speicherort, in dem Sie das Beispiel gespeichert haben, klicken Sie auf **mrxp32.vcproj**und klicken Sie dann auf **Öffnen**.
    
7. Klicken Sie im Menü **Erstellen** auf **Konfigurations-Manager**.
    
8. Klicken Sie im Dialogfeld **Konfigurations-Manager** wechseln Sie in der Zeile **mrxp32** in der Spalte **Konfiguration** wählen Sie **Release aus**und klicken Sie dann auf **Schließen**.
    
9. On the **Build** menu, click **Build Solution**.
    
10. Klicken Sie im Dialogfeld **Datei speichern unter** auf **Speichern**.
    
11. In den Ordner, in dem Sie das Beispiel gespeichert haben, mit der rechten Maustaste der Installations-Batchdatei, und klicken Sie auf **als Administrator ausführen**.
    
12. Klicken Sie im Dialogfeld **Benutzerkontensteuerung** auf **Weiter**.
    
    > [!NOTE]
    > **Install.bat** kopiert die DLL-Datei in den standardmäßigen Microsoft Office-Installationsordner C:\Program Files\Microsoft Office\Office12\. Wenn Sie Office-Produkte an einem anderen Speicherort installiert haben, mit der rechten Maustaste **Install.bat aus** , und klicken Sie auf **Bearbeiten**. Die Datei wird im Editor geöffnet. Ersetzen Sie den Standardpfad für die Installation durch den Installationspfad auf Ihrem Computer verwendet. 
  
 **Einrichten der Adressbuchhierarchie in Outlook**
  
1. Klicken Sie auf von Outlook im Menü **Extras** auf **Konten-Einstellungen**.
    
2. Klicken Sie im Dialogfeld **Kontoeinstellungen** auf der Registerkarte **E-Mail** auf **neu**.
    
3. Klicken Sie unter **E-Mail-Dienst auswählen** auf **andere**, wählen Sie **MRXP Beispiel Transport aus**, und klicken Sie dann auf **Weiter**.
    
4. Geben Sie im Dialogfeld **MRXP Transportkonfiguration** einen **Anzeigenamen des Benutzers ein**.
    
5. Geben Sie unter **Pfad zur Posteingang (UNC-Freigabe)** einen Ordnerpfad aus. Dies kann auch ein Pfad zu einem lokalen Ordner sein. 
    
    > [!IMPORTANT]
    > In diesem Pfad muss vorhanden sein. 
  
6. Klicken Sie auf **OK**.
    
7. Klicken Sie im Dialogfeld **E-Mail-Konto hinzufügen** auf **OK**. Klicken Sie auf **Fertig stellen** , und klicken Sie dann auf **Schließen**.
    
8. Um mit dem Konto MRXP zu starten, beenden und starten Sie Outlook neu.
    
 **So verwenden Sie Sample Anbieter Transport zum Senden einer Nachricht in Outlook**
  
1. Klicken Sie im Menü **Datei** auf **neu**und klicken Sie dann auf **E-Mail-Nachricht**.
    
2. Geben Sie in das Feld **an** den Namen des Empfängers mit dem Format **[MRXP:\<Adresse\>]**. Die Adresse ist der UNC-Freigabe oder lokalen Ordnerpfad an den Posteingang des Empfängers.
    
    > [!NOTE]
    > Doppelpunkte oder umgekehrte Schrägstriche in der Adresse vorhanden sind, müssen Sie einen umgekehrten Schrägstrich vor jeder Doppelpunkt oder umgekehrten Schrägstrich einfügen. Beispielsweise zum Senden von e-Mails an [MRXP:C:\Mail\myDir] Geben Sie `[MRXP:C\:\\Mail\\myDir]`. 
  
    > [!IMPORTANT]
    > Die Adresse des Empfängers muss vorhanden sein. 
  
3. Klicken Sie auf **Konto** , und klicken Sie dann auf **MRXP Beispiel Transport**.
    
4. Geben Sie Ihre Nachricht ein, und klicken Sie auf **Senden**. Die Nachricht wird mithilfe der Adressbuchhierarchie MRXP gesendet.
    
 **Zum Verwenden des Transport-Anbieter-Beispiels zum Empfangen einer Nachricht in Outlook**
  
1. Klicken Sie im Menü **Datei** auf **neu**und klicken Sie dann auf **E-Mail-Nachricht**.
    
2. Geben Sie Ihre Nachricht ein.
    
3. Klicken Sie auf der **Microsoft Office-Schaltfläche**, klicken Sie auf **Speichern unter**, und klicken Sie dann auf **Speichern unter,** um die Datei in den Posteingangsordner zu speichern, die Sie während der Installation angegeben. 
    
4. Klicken Sie im Dialogfeld **Speichern unter,** wechseln Sie zu den UNC-Freigabe oder einem lokalen Ordner, den im Posteingang festgelegt. 
    
5. Klicken Sie im Dropdown **Dateityp** - **Outlook-Nachrichtenformat**auf.
    
6. Geben Sie einen Namen für die Datei, und klicken Sie auf **Speichern**.
    
7. Die Datei wird in den freigegebenen Ordner gespeichert. Der Transportdienst MRXP übermittelt die Nachricht an Ihren Posteingang in Outlook.
    

