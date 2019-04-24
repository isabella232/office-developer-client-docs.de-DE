---
title: Beispiel für einen Transport Anbieter
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ec6eb6c0-bfe3-4989-9071-89a14c0e7bdd
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: def51a752abcb79a35980ed12eb73011c26d2597
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356588"
---
# <a name="transport-provider-sample"></a>Beispiel für einen Transport Anbieter

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
In diesem Beispiel werden Dateien und Verzeichnisse zum Senden und empfangen von Nachrichten verwendet. Es wird ein sehr einfacher Präprozessor implementiert und registriert, der jeder ausgehenden Nachricht eine Textzeile hinzufügt. Im Beispiel wird veranschaulicht, wie der Nachrichteninhalt zwischen dem Transport Neutral Encapsulation Format (TNEF) und dem Text geteilt wird. Außerdem werden alle Konfigurationsoptionen (Eigenschaftenblätter, Assistenten und programmgesteuerte Konfiguration) und Nachrichtenoptionen unterstützt. Die Remote Transport Schnittstellen werden nicht unterstützt. 
  
Sie können dieses Beispiel aus [MAPI-Code Beispielen (Outlook Messaging API)](https://go.microsoft.com/fwlink/?LinkId=129740)herunterladen.
  
|||
|:-----|:-----|
|Executable  <br/> |mrxp32. dll  <br/> |
|Quellcodeverzeichnis:  <br/> |SampleTransportProvider\MRXP  <br/> |
|Sprache  <br/> |C++  <br/> |
|Plattformen  <br/> |Visual Studio 2008 für die Kompilierung für Windows Vista, Windows Server 2008, Windows XP SP2 und Windows Server 2003 SP1  <br/> |
   
## <a name="supported-features"></a>Unterstützte Features

In diesem Beispiel werden die folgenden Features unterstützt:
  
- Grundlegende Features wie senden, empfangen und Abrufen von neuen Nachrichten.
    
- Interaktive und programmgesteuerte Konfiguration.
    
- Die **IMAPIStatus** -Schnittstelle, mit Ausnahme der Eigenschaftseinstellung. Weitere Informationen finden Sie unter der [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) -Schnittstelle. 
    
- Thread Sicherheit.
    
- Ereignisprotokollierung in eine Textdatei. Die Datei wird automatisch auf eine bestimmte Größe beschränkt. Alle Transportsitzungen verwenden dieselbe Datei.
    
## <a name="unsupported-features"></a>Nicht unterstützte Features

In diesem Beispiel wird die asynchrone Erkennung eingehender Nachrichten nicht unterstützt.
  
 **So installieren Sie den Beispiel Transport Anbieter**
  
1. Informationen zum Herunterladen des Beispiel Transport Anbieters finden Sie unter [herunterladen der Outlook-MAPI-Beispiele](downloading-the-outlook-mapi-samples.md).
    
2. Suchen Sie den Ordner, in dem Sie die Outlook-MAPI-Beispiele gespeichert haben. Klicken Sie mit der rechten Maustaste auf den Zip **-Ordner OutlookMAPISamples-\<Versions\> Nummer** , und klicken Sie auf **Alle extrahieren**.
    
3. Klicken Sie auf **Durchsuchen**, wählen Sie den Speicherort aus, an dem Sie das Beispiel speichern möchten, und klicken Sie auf **extrahieren**.
    
4. Führen Sie Visual Studio 2008 aus.
    
5. Klicken Sie in Visual Studio 2008 auf **Datei**, wählen Sie **Öffnen**aus, und klicken Sie dann auf **Projekt/Lösung**.
    
6. Navigieren Sie zu dem Speicherort, an dem Sie das Beispiel gespeichert haben, klicken Sie auf **mrxp32. vcproj**, und klicken Sie dann auf **Öffnen**.
    
7. Klicken Sie im Menü **Erstellen** auf **Konfigurations-Manager**.
    
8. Wechseln Sie im Dialogfeld **Konfigurations-Manager** zur Zeile **mrxp32** , und wählen Sie in der Spalte **Konfiguration** die Option **Release**aus, und klicken Sie dann auf **Schließen**.
    
9. On the **Build** menu, click **Build Solution**.
    
10. Klicken Sie im Dialogfeld **Datei speichern** unter auf **Speichern**.
    
11. Klicken Sie in dem Ordner, in dem Sie das Beispiel gespeichert haben, mit der rechten Maustaste auf die Installationsbatchdatei, und klicken Sie dann auf **als Administrator ausführen**.
    
12. Klicken Sie im Dialogfeld **Benutzerkontensteuerung** auf **Weiter**.
    
    > [!NOTE]
    > **install. bat** kopiert die dll in den standardMäßigen Microsoft Office-Installationsordner, c:\Programme\Microsoft Office\Office12\. Wenn Sie Office-Produkte an einem anderen Speicherort installiert haben, klicken Sie mit der rechten Maustaste auf **install. bat** , und klicken Sie auf **Bearbeiten**. Die Datei wird im Editor geöffnet. Ersetzen Sie den Standardinstallationspfad durch den Installationspfad, der auf Ihrem Computer verwendet wird. 
  
 **So richten Sie den Transport Anbieter in Outlook ein**
  
1. Klicken Sie im Menü **Extras** von Outlook auf **Kontoeinstellungen**.
    
2. Klicken Sie im Dialogfeld **Kontoeinstellungen** auf der Registerkarte **e-Mail** auf **neu**.
    
3. Klicken Sie unter **e-Mail-Dienst auswählen** auf **Sonstiges**, wählen Sie **MRXP-Beispiel Transport**aus, und klicken Sie dann auf **weiter**.
    
4. Geben Sie im Dialogfeld **MRXP-Transport Konfiguration** einen **Benutzeranzeigenamen**ein.
    
5. Geben Sie unter **Pfad zu Posteingang (UNC-Freigabe)** einen Ordnerpfad ein. Dabei kann es sich auch um einen Pfad zu einem lokalen Ordner handeln. 
    
    > [!IMPORTANT]
    > Dieser Pfad muss vorhanden sein. 
  
6. Klicken Sie auf **OK**.
    
7. Klicken Sie im Dialogfeld **e-Mail-Konto hinzufügen** auf **OK**. Klicken Sie auf **Fertig stellen** und dann auf **Schließen**.
    
8. Beenden Sie Outlook, und starten Sie es neu, um das MRXP-Konto zu verwenden.
    
 **So verwenden Sie das Transport Anbieterbeispiel zum Senden einer Nachricht in Outlook**
  
1. Klicken Sie im Menü **Datei** auf **neu**, und klicken Sie dann auf **e-Mail-Nachricht**.
    
2. Geben Sie im Feld **an** den Namen des Empfängers mit dem Format **[MRXP:\<Address\>]** ein. Die Adresse ist die UNC-Freigabe oder der lokale Ordnerpfad zum Posteingang des Empfängers.
    
    > [!NOTE]
    > Wenn die Adresse Doppelpunkte oder umgekehrte Schrägstriche enthält, müssen Sie vor jedem Doppelpunkt oder Backslash einen umgekehrten Schrägstrich einfügen. Wenn Sie beispielsweise eine e-Mail an [MRXP: C: \Mail\myDir] senden möchten, `[MRXP:C\:\\Mail\\myDir]`müssen Sie Folgendes eingeben. 
  
    > [!IMPORTANT]
    > Die Empfängeradresse muss vorhanden sein. 
  
3. Klicken Sie auf **Konto** , und klicken Sie dann auf **MRXP-Beispiel Transport**.
    
4. Geben Sie Ihre Nachricht ein, und klicken Sie auf **senden**. Die Nachricht wird mit dem MRXP-Transportanbieter gesendet.
    
 **So verwenden Sie das Transport Anbieterbeispiel zum Empfangen einer Nachricht in Outlook**
  
1. Klicken Sie im Menü **Datei** auf **neu**, und klicken Sie dann auf **e-Mail-Nachricht**.
    
2. Geben Sie Ihre Nachricht ein.
    
3. Klicken Sie auf die **Microsoft Office-Schaltfläche**, klicken Sie auf **Speichern**unter, und klicken Sie dann auf **Speichern** unter, um die Datei im Posteingang-Ordner zu speichern, den Sie während der Installation angegeben haben 
    
4. Navigieren Sie im Dialogfeld **Speichern** unter zu der UNC-Freigabe oder dem lokalen Ordner, den Sie als Posteingang festgelegt haben. 
    
5. Klicken Sie **** im Dropdownmenü Dateityp auf Outlook- **Nachrichten Format**.
    
6. Geben Sie einen Namen für die Datei ein, und klicken Sie auf **Speichern**.
    
7. Die Datei wird im freigegebenen Ordner gespeichert. Der MRXP-Transportanbieter übermittelt die Nachricht in Outlook an Ihren Posteingang.
    

