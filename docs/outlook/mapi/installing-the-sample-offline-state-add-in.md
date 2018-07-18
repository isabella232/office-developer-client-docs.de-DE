---
title: Installieren des Offlinestatus-Add-In-Beispiels
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1b6ae6c-dcf2-a07f-c417-3a1049b758ad
description: 'Zuletzt geändert: 06 Juli 2012'
ms.openlocfilehash: 00232f290c367c4bab1854bfe3909abc7b03cef8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792715"
---
# <a name="installing-the-sample-offline-state-add-in"></a>Installieren des Offlinestatus-Add-In-Beispiels

  
  
**Betrifft**: Outlook 
  
In diesem Thema führt Sie durch die Schritte zum Herunterladen und Offline-Status Beispiel-Add-in installieren. Das Offline-Status Beispiel-Add-in ist ein COM-add-in, die ein Menü **Status als offline anzeigen** zu Outlook hinzugefügt und State-API verwendet. Überprüfen Sie über das Menü Offline-Status, das können Sie aktivieren oder deaktivieren, Status der Überwachung den aktuellen Status, und ändern Sie den aktuellen Status. Weitere Informationen dazu, wie das Offline-Status-Add-in implementiert wird finden Sie unter [Einstellung Up eine Offline-Status-Add-in](setting-up-an-offline-state-add-in.md).
  
## <a name="install-the-sample-offline-state-add-in"></a>Installieren Sie das Beispiel Offline State-Add-in

1. Das Beispiel Offline Zustand Add-in hier herunterladen: [Outlook 2007: zusätzliche Referenzcodebeispiele und verteilbares Installationsprogramm](http://www.microsoft.com/en-us/download/details.aspx?id=24102).
    
2. Visual Studio 2005 als Administrator ausführen.
    
    > [!NOTE]
    > Wenn Ihr Computer unter Windows XP ausgeführt wird, müssen Sie als Administrator angemeldet sein,. Wenn Ihr Computer Windows Vista ausgeführt wird, müssen Sie als Administrator angemeldet sein,. Mit der rechten Maustaste in des Visual Studio 2005-Symbols, und klicken Sie auf **als Administrator ausführen**. 
  
3. Klicken Sie in Visual Studio 2005 auf **Datei**, klicken Sie auf **Öffnen**, und klicken Sie dann auf **Projekt/Projektmappe**.
    
4. Navigieren Sie zum Speicherort, in dem Sie das Beispiel gespeichert haben, klicken Sie auf **ConnectionStateAddin**und klicken Sie dann auf **Öffnen**.
    
5. On the **Build** menu, click **Build Solution**.
    
6. Klicken Sie im Dialogfeld **Datei speichern unter** auf **Speichern**.
    
7. Klicken Sie auf **das Startmenü** , klicken Sie auf **Alle Programme**, klicken Sie auf **Zubehör**, mit der rechten Maustaste **an der Eingabeaufforderung**, und klicken Sie dann auf **als Administrator ausführen**.
    
    > [!NOTE]
    > Wenn Sie Windows XP ausgeführt werden, müssen Sie als Administrator angemeldet sein,. 
  
8. Klicken Sie im Dialogfeld **Benutzerkontensteuerung** auf **Weiter**.
    
9. Wechseln Sie in **das Eingabeaufforderungsfenster** zum Ordner "Debug", in dem Sie das Beispiel gespeichert haben. Wenn Sie das Beispiel auf Laufwerk C:\ gespeichert, würden Sie beispielsweise geben Sie **cd "C:\ConnectionStateAddin\Debug"** und **dann die EINGABETASTE**. 
    
10. Geben Sie **regsvr32 OfflineStateAddin.dll** ein, und drücken Sie die **EINGABETASTE**. 
    
    > [!NOTE]
    > Um das Beispiel Offline Zustand-Add-in zu deinstallieren, geben Sie **regsvr32 -u OfflineStateAddin.dll**
  
11. Klicken Sie im Dialogfeld **RegSrv32** klicken Sie auf **OK**.
    
12. Starten Sie Outlook, um das Menü **Status als Offline** angezeigt. 
    
## <a name="see-also"></a>Siehe auch



[Informationen zu der Offlinestatus-API](about-the-offline-state-api.md)
  
[Installieren des Offlinestatus-Add-In-Beispiels](installing-the-sample-offline-state-add-in.md)
  
[Informationen zum Offlinestatus-Add-In-Beispiel](about-the-sample-offline-state-add-in.md)
  
[Einrichten eines Offlinestatus-Add-Ins](setting-up-an-offline-state-add-in.md)
  
[Überwachen von Verbindungsstatusänderungen mit einem Offlinestatus-Add-In](monitoring-connection-state-changes-using-an-offline-state-add-in.md)
  
[Trennen eines Offlinestatus-Add-Ins](disconnecting-an-offline-state-add-in.md)

