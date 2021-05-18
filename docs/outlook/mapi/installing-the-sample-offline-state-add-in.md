---
title: Installieren des Beispiel-Offlinestatus-Add-Ins
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1b6ae6c-dcf2-a07f-c417-3a1049b758ad
description: 'Letzte Änderung: 06. Juli 2012'
ms.openlocfilehash: b7b9ce539537e0759020ef7e3b4f6541a940d6fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317213"
---
# <a name="installing-the-sample-offline-state-add-in"></a>Installieren des Beispiel-Offlinestatus-Add-Ins

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
In diesem Thema werden Die Schritte zum Herunterladen und Installieren des Beispiel-Offlinestatus-Add-Ins beschrieben. Das Beispiel-Offlinestatus-Add-In ist ein COM-Add-In, das ein **Offlinestatusmenü** zu Outlook und die Offlinestatus-API verwendet. Über das Menü Offlinestatus können Sie die Zustandsüberwachung aktivieren oder deaktivieren, den aktuellen Status überprüfen und den aktuellen Status ändern. Weitere Informationen zur Implementierung des Offlinestatus-Add-Ins finden Sie unter [Einrichten eines Offlinestatus-Add-Ins.](setting-up-an-offline-state-add-in.md)
  
## <a name="install-the-sample-offline-state-add-in"></a>Installieren des Beispiel-Offlinestatus-Add-Ins

1. Laden Sie das Beispiel-Offlinestatus-Add-In hier herunter: [Outlook 2007 Auxiliary Reference Code Samples and Redistributable Installer](https://www.microsoft.com/en-us/download/details.aspx?id=24102).
    
2. Führen Visual Studio 2005 als Administrator aus.
    
    > [!NOTE]
    > Wenn Ihr Computer mit Windows XP ausgeführt wird, müssen Sie als Administrator angemeldet sein. Wenn Ihr Computer Windows Vista ausgeführt wird, müssen Sie als Administrator angemeldet sein. Klicken Sie mit der rechten Maustaste auf Visual Studio 2005-Symbol, und klicken Sie **auf Als Administrator ausführen**. 
  
3. Klicken Visual Studio 2005 auf **Datei,** wählen Sie **Öffnen** aus, und klicken Sie **dann auf Project/Lösung**.
    
4. Navigieren Sie zu dem Speicherort, an dem Sie das Beispiel gespeichert haben, klicken Sie auf **ConnectionStateAddin**, und klicken Sie dann auf **Öffnen**.
    
5. On the **Build** menu, click **Build Solution**.
    
6. Klicken Sie im Dialogfeld Datei speichern **unter** auf **Speichern**.
    
7. Klicken Sie auf das Menü  **Start,** klicken Sie auf **Alle Programme,** klicken Sie auf **Zubehör,** klicken Sie mit der rechten Maustaste auf Eingabeaufforderung, und klicken Sie dann auf Als Administrator ausführen . 
    
    > [!NOTE]
    > Wenn Sie xp Windows, müssen Sie als Administrator angemeldet sein. 
  
8. Klicken Sie im Dialogfeld **Benutzerkontensteuerung** auf **Weiter**.
    
9. Ändern Sie **im Eingabeaufforderungsfenster** Verzeichnisse in den Ordner Debuggen, in dem Sie das Beispiel gespeichert haben. Wenn Sie z. B. das Beispiel auf Ihrem C:\ gespeichert haben geben Sie cd **"C:\ConnectionStateAddin\Debug"** ein, und drücken Sie dann die **EINGABETASTE**. 
    
10. Geben **Sie regsvr32 OfflineStateAddin.dll** ein, und drücken Sie die **EINGABETASTE.** 
    
    > [!NOTE]
    > Geben Sie zum Deinstallieren des Beispiel-Offlinestatus-Add-Ins **regsvr32 -u OfflineStateAddin.dll**
  
11. Klicken Sie **im Dialogfeld RegSrv32** auf **OK**.
    
12. Starten Outlook, um das Menü **Offlinestatus anzuzeigen.** 
    
## <a name="see-also"></a>Siehe auch



[Informationen zur Offlinestatus-API](about-the-offline-state-api.md)
  
[Installieren des Offlinestatus-Add-In-Beispiels](installing-the-sample-offline-state-add-in.md)
  
[Informationen zum Offlinestatus-Add-In-Beispiel](about-the-sample-offline-state-add-in.md)
  
[Einrichten eines Offlinestatus-Add-Ins](setting-up-an-offline-state-add-in.md)
  
[Überwachen von Verbindungsstatusänderungen mit einem Offlinestatus-Add-In](monitoring-connection-state-changes-using-an-offline-state-add-in.md)
  
[Trennen der Trennung eines Offlinestatus-Add-Ins](disconnecting-an-offline-state-add-in.md)

