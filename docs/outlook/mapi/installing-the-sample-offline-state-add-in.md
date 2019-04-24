---
title: Installieren des Offline Status-Beispiel-Add-ins
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1b6ae6c-dcf2-a07f-c417-3a1049b758ad
description: 'Zuletzt geändert: 06 Juli, 2012'
ms.openlocfilehash: b7b9ce539537e0759020ef7e3b4f6541a940d6fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317213"
---
# <a name="installing-the-sample-offline-state-add-in"></a>Installieren des Offline Status-Beispiel-Add-ins

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
In diesem Thema werden die Schritte zum herunterladen und Installieren des Offline Status-Add-in-Beispiels erläutert. Das Beispiel für Offlinestatus-Add-in ist ein COM-Add-in, das ein **Offlinestatus** Menü zu Outlook hinzufügt und die OFFLINESTATUS-API verwendet. Über das Offline Status Menü können Sie die Statusüberwachung aktivieren oder deaktivieren, den aktuellen Status überprüfen und den aktuellen Status ändern. Weitere Informationen dazu, wie das Offlinestatus-Add-in implementiert wird, finden Sie unter [Einrichten eines Offlinestatus-Add-ins](setting-up-an-offline-state-add-in.md).
  
## <a name="install-the-sample-offline-state-add-in"></a>Installieren des Offline Status-Beispiel-Add-ins

1. Laden Sie sich das Beispiel für das Offline Status-Add-in hier herunter: [Outlook 2007 Auxiliary Reference Code Samples und redistributAble Installer](https://www.microsoft.com/en-us/download/details.aspx?id=24102).
    
2. Führen Sie Visual Studio 2005 als Administrator aus.
    
    > [!NOTE]
    > Wenn auf Ihrem Computer Windows XP läuft, müssen Sie als Administrator angemeldet sein. Wenn auf Ihrem Computer Windows Vista installiert ist, müssen Sie als Administrator angemeldet sein. Klicken Sie mit der rechten Maustaste auf das Visual Studio 2005-Symbol, und klicken Sie auf **als Administrator ausführen**. 
  
3. Klicken Sie in Visual Studio 2005 auf **Datei**, wählen Sie **Öffnen**aus, und klicken Sie dann auf **Projekt/Lösung**.
    
4. Navigieren Sie zu dem Speicherort, an dem Sie das Beispiel gespeichert haben, klicken Sie auf **ConnectionStateAddin**, und klicken Sie dann auf **Öffnen**.
    
5. On the **Build** menu, click **Build Solution**.
    
6. Klicken Sie im Dialogfeld **Datei speichern** unter auf **Speichern**.
    
7. Klicken Sie im **Startmenü** auf **Alle Programme**, klicken Sie auf **Zubehör**, klicken Sie mit der rechten Maustaste auf **Eingabeaufforderungen**, und klicken Sie dann auf **als Administrator ausführen**.
    
    > [!NOTE]
    > Wenn Sie Windows XP betreiben, müssen Sie als Administrator angemeldet sein. 
  
8. Klicken Sie im Dialogfeld **Benutzerkontensteuerung** auf **Weiter**.
    
9. Ändern Sie im **Eingabe Aufforderungs** Fenster die Verzeichnisse in den Debug-Ordner, in dem Sie das Beispiel gespeichert haben. Wenn Sie beispielsweise das Beispiel in der Datei "c:" gespeichert haben, **"C:\ConnectionStateAddin\Debug"** , und drücken Sie dann die **Eingabe**Taste. 
    
10. Geben Sie **regsvr32 OfflineStateAddin. dll** ein, und drücken **Sie die Eingabe**Taste. 
    
    > [!NOTE]
    > Zum Deinstallieren des Beispiel-Offline Status-Add-ins geben Sie **regsvr32-u OfflineStateAddin. dll ein.**
  
11. Klicken Sie im Dialogfeld **RegSrv32** auf **OK**.
    
12. Starten Sie Outlook neu, um das **Offline Status** Menü anzuzeigen. 
    
## <a name="see-also"></a>Siehe auch



[Informationen zur Offlinestatus-API](about-the-offline-state-api.md)
  
[Installieren des Offlinestatus-Add-In-Beispiels](installing-the-sample-offline-state-add-in.md)
  
[Informationen zum Offlinestatus-Add-In-Beispiel](about-the-sample-offline-state-add-in.md)
  
[Einrichten eines Offlinestatus-Add-Ins](setting-up-an-offline-state-add-in.md)
  
[Überwachen von Verbindungsstatusänderungen mit einem Offlinestatus-Add-In](monitoring-connection-state-changes-using-an-offline-state-add-in.md)
  
[Trennen eines Offline Status-Add-ins](disconnecting-an-offline-state-add-in.md)

