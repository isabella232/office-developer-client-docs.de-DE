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
ms.openlocfilehash: def51a752abcb79a35980ed12eb73011c26d2597
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356588"
---
# <a name="transport-provider-sample"></a>Beispiel für einen Transportanbieter

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
In diesem Beispiel werden Dateien und Verzeichnisse zum Übertragen und Empfangen von Nachrichten verwendet. Es implementiert und registriert einen sehr einfachen Präprozessor, der jeder ausgehenden Nachricht eine Textzeile anfügen kann. Das Beispiel veranschaulicht, wie Nachrichteninhalte zwischen TNEF (Transport Neutral Encapsulation Format) und Text aufgeteilt werden. Außerdem werden alle Konfigurationsoptionen (Eigenschaftenblätter, Assistenten und programmgesteuerte Konfiguration) und Nachrichtenoptionen unterstützt. Die Remote-Transportschnittstellen werden nicht unterstützt. 
  
Sie können dieses Beispiel aus Outlook [Messaging-API (MAPI)-Codebeispiele herunterladen.](https://go.microsoft.com/fwlink/?LinkId=129740)
  
|||
|:-----|:-----|
|Ausführbare Datei:  <br/> |mrxp32.dll  <br/> |
|Quellcodeverzeichnis:  <br/> |SampleTransportProvider\MRXP  <br/> |
|Sprache:  <br/> |C++  <br/> |
|Plattformen:  <br/> |Visual Studio 2008 zum Kompilieren für Windows Vista, Windows Server 2008, Windows XP SP2 und Windows Server 2003 SP1  <br/> |
   
## <a name="supported-features"></a>Unterstützte Features

Dieses Beispiel unterstützt die folgenden Features:
  
- Grundlegende Features wie das Senden, Empfangen und Abrufen neuer Nachrichten.
    
- Interaktive und programmgesteuerte Konfiguration.
    
- Die **IMAPIStatus-Schnittstelle,** mit Ausnahme der Eigenschafteneinstellung. Weitere Informationen finden Sie unter [IMAPIStatus : IMAPIProp-Schnittstelle.](imapistatusimapiprop.md) 
    
- Threadsicherheit.
    
- Ereignisprotokollierung bei einer Textdatei. Die Datei ist automatisch auf eine angegebene Größe beschränkt. Alle Transportsitzungen verwenden dieselbe Datei.
    
## <a name="unsupported-features"></a>Nicht unterstützte Features

Dieses Beispiel unterstützt keine asynchrone Erkennung eingehender Nachrichten.
  
 **So installieren Sie den Beispieltransportanbieter**
  
1. Informationen zum Herunterladen des Beispieltransportanbieters finden Sie unter [Herunterladen der Outlook MAPI-Beispiele](downloading-the-outlook-mapi-samples.md).
    
2. Suchen Sie den Ordner, in dem Sie die Outlook gespeichert haben. Klicken Sie mit der rechten Maustaste auf den **Ordner OutlookMAPISamples- \< version number \>** zip, und klicken Sie auf Alle **extrahieren.**
    
3. Klicken **Sie auf Durchsuchen,** wählen Sie den Speicherort aus, an dem Sie das Beispiel speichern möchten, und klicken Sie auf **Extrahieren**.
    
4. Führen Visual Studio 2008 aus.
    
5. Klicken Visual Studio 2008 auf **Datei,** wählen Sie **Öffnen** aus, und klicken Sie **dann auf Project/Lösung**.
    
6. Navigieren Sie zu dem Speicherort, an dem Sie das Beispiel gespeichert haben, klicken Sie **auf mrxp32.vcproj,** und klicken Sie dann auf **Öffnen**.
    
7. Klicken Sie **im Menü** Erstellen auf **Configuration Manager**.
    
8. Wechseln Sie im Dialogfeld **Configuration Manager** zur **Zeile mrxp32,** und wählen Sie in der Spalte **Konfiguration** die Option **Release** aus, und klicken Sie dann auf **Schließen**.
    
9. On the **Build** menu, click **Build Solution**.
    
10. Klicken Sie im Dialogfeld Datei speichern **unter** auf **Speichern**.
    
11. Klicken Sie im Ordner, in dem Sie das Beispiel gespeichert haben, mit der rechten Maustaste auf die Installationsbatchdatei, und klicken Sie **auf Als Administrator ausführen**.
    
12. Klicken Sie im Dialogfeld **Benutzerkontensteuerung** auf **Weiter**.
    
    > [!NOTE]
    > **install.bat** kopiert die .dll in den Standardinstallationsordner Microsoft Office C:\Program Files\Microsoft Office\Office12\. Wenn Sie die Office an einem anderen Speicherort installiert haben, klicken Sie mit der rechten Maustaste **aufinstall.bat** und klicken Sie auf **Bearbeiten**. Die Datei wird in Editor. Ersetzen Sie den Standardinstallationspfad durch den Installationspfad, der auf Ihrem Computer verwendet wird. 
  
 **So richten Sie den Transportanbieter in Outlook**
  
1. Klicken Sie **im** Menü Extras Outlook auf **Konto Einstellungen**.
    
2. Klicken Sie **im Einstellungen** Auf **der** Registerkarte E-Mail auf **Neu**.
    
3. Klicken **Sie unter E-Mail-Dienst** auswählen **auf Andere,** wählen **Sie MRXP-Beispieltransport** aus, und klicken Sie dann auf **Weiter**.
    
4. Geben Sie **im Dialogfeld MRXP-Transportkonfiguration** einen **Benutzeranzeigenamen ein.**
    
5. Geben **Sie unter Pfad zum Posteingang (UNC Share)** einen Ordnerpfad ein. Dies kann auch ein Pfad zu einem lokalen Ordner sein. 
    
    > [!IMPORTANT]
    > Dieser Pfad muss vorhanden sein. 
  
6. Klicken Sie auf **OK**.
    
7. Klicken Sie **im Dialogfeld E-Mail-Konto** hinzufügen auf **OK**. Klicken Sie **auf Fertig** stellen, und klicken Sie dann auf **Schließen**.
    
8. Um mit der Verwendung des MRXP-Kontos zu beginnen, beenden und starten Sie Outlook.
    
 **So verwenden Sie das Beispiel des Transportanbieters zum Senden einer Nachricht in Outlook**
  
1. Klicken Sie **im** Menü Datei auf **Neu,** und klicken Sie dann auf **E-Mail-Nachricht**.
    
2. Geben Sie **im Feld An** den Namen des Empfängers im Format **[MRXP: \< ADDRESS ] \> ein.** Die Adresse ist der UNC-Freigabe- oder lokaler Ordnerpfad zum Posteingang des Empfängers.
    
    > [!NOTE]
    > Wenn die Adresse Doppelpunkte oder umgekehrte Schrägstriche hat, müssen Sie vor jedem Doppelpunkt oder umgekehrten Schrägstrich einen umgekehrten Schrägstrich einfügen. Zum Senden von E-Mails an [MRXP:C:\Mail\myDir] müssen Sie z. B.  `[MRXP:C\:\\Mail\\myDir]` eingeben. 
  
    > [!IMPORTANT]
    > Die Empfängeradresse muss vorhanden sein. 
  
3. Klicken Sie **auf Konto,** und klicken Sie dann **auf MRXP-Beispieltransport**.
    
4. Geben Sie Ihre Nachricht ein, und klicken Sie auf **Senden**. Die Nachricht wird über den MRXP-Transportanbieter gesendet.
    
 **So verwenden Sie das Beispiel des Transportanbieters zum Empfangen einer Nachricht in Outlook**
  
1. Klicken Sie **im** Menü Datei auf **Neu,** und klicken Sie dann auf **E-Mail-Nachricht**.
    
2. Geben Sie Ihre Nachricht ein.
    
3. Klicken Sie **Microsoft Office Schaltfläche,** klicken Sie auf **Speichern unter**, und klicken Sie dann auf **Speichern unter,** um die Datei im Posteingangsordner zu speichern, den Sie während des Setups angegeben haben. 
    
4. Navigieren Sie **im** Dialogfeld Speichern unter zu der UNC-Freigabe oder dem lokalen Ordner, den Sie als Posteingang festlegen. 
    
5. Klicken Sie **in der Dropdownliste** Unter Typ speichern **auf Outlook Nachrichtenformat**.
    
6. Geben Sie einen Namen für die Datei ein, und klicken Sie auf **Speichern**.
    
7. Die Datei wird im freigegebenen Ordner gespeichert. Der MRXP-Transportanbieter übermittelt die Nachricht an Ihren Posteingang in Outlook.
    

