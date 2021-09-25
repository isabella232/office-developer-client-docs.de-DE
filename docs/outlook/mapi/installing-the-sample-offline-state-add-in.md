---
title: Installieren des Offlinestatus-Beispiel-Add-Ins
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: e1b6ae6c-dcf2-a07f-c417-3a1049b758ad
description: 'Last modified: July 06, 2012'
ms.openlocfilehash: f57055c0c9b5651023f110e9540a49382f275696
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630438"
---
# <a name="installing-the-sample-offline-state-add-in"></a>Installieren des Offlinestatus-Beispiel-Add-Ins

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
In diesem Thema werden sie durch die Schritte zum Herunterladen und Installieren des Offlinestatus-Beispiel-Add-Ins geführt. Das Offlinestatus-Beispiel-Add-In ist ein COM-Add-In, das Outlook ein **Offlinestatusmenü** hinzufügt und die Offlinestatus-API verwendet. Über das Menü "Offlinestatus" können Sie die Zustandsüberwachung aktivieren oder deaktivieren, den aktuellen Status überprüfen und den aktuellen Status ändern. Weitere Informationen zur Implementierung des Offlinestatus-Add-Ins finden Sie unter [Einrichten eines Offlinestatus-Add-Ins.](setting-up-an-offline-state-add-in.md)
  
## <a name="install-the-sample-offline-state-add-in"></a>Installieren des Offlinestatus-Beispiel-Add-Ins

1. Laden Sie das Beispiel-Offlinestatus-Add-In hier herunter: [Outlook 2007 Auxiliary Reference Code Samples and Redistributable Installer](https://www.microsoft.com/en-us/download/details.aspx?id=24102).
    
2. Führen Sie Visual Studio 2005 als Administrator aus.
    
    > [!NOTE]
    > Wenn Ihr Computer Windows XP ausgeführt wird, müssen Sie als Administrator angemeldet sein. Wenn Ihr Computer Windows Vista ausgeführt wird, müssen Sie als Administrator angemeldet sein. Klicken Sie mit der rechten Maustaste auf das Symbol Visual Studio 2005, und klicken Sie auf **"Als Administrator ausführen".** 
  
3. Klicken Sie in Visual Studio 2005 auf **"Datei",** wählen Sie **"Öffnen"** aus, und klicken Sie dann auf **Project/Lösung.**
    
4. Navigieren Sie zu dem Speicherort, an dem Sie das Beispiel gespeichert haben, klicken Sie auf **"ConnectionStateAddin",** und klicken Sie dann auf **"Öffnen".**
    
5. On the **Build** menu, click **Build Solution**.
    
6. Klicken Sie im Dialogfeld **"Datei speichern unter"** auf **"Speichern".**
    
7. Klicken Sie auf das **Startmenü,** klicken Sie auf **"Alle Programme",** klicken Sie auf **"Zubehör",** klicken Sie mit der rechten Maustaste auf **"Eingabeaufforderung"** und dann auf **"Als Administrator ausführen".**
    
    > [!NOTE]
    > Wenn Sie Windows XP ausführen, müssen Sie als Administrator angemeldet sein. 
  
8. Klicken Sie im Dialogfeld **Benutzerkontensteuerung** auf **Weiter**.
    
9. Ändern Sie im **Eingabeaufforderungsfenster** die Verzeichnisse in den Debugordner, in dem Sie das Beispiel gespeichert haben. Wenn Sie das Beispiel beispielsweise in Ihrem C:\ gespeichert haben Geben Sie **cd "C:\ConnectionStateAddin\Debug"** ein, und drücken Sie dann die **EINGABETASTE.** 
    
10. Geben Sie **regsvr32 OfflineStateAddin.dll** ein, und drücken Sie die **EINGABETASTE.** 
    
    > [!NOTE]
    > Um das Offlinestatus-Beispiel-Add-In zu deinstallieren, geben Sie **regsvr32 -u OfflineStateAddin.dll**
  
11. Klicken Sie im Dialogfeld **RegSrv32** auf **OK.**
    
12. Starten Sie Outlook neu, um das **Offlinestatusmenü** anzuzeigen. 
    
## <a name="see-also"></a>Siehe auch



[Informationen zur Offlinestatus-API](about-the-offline-state-api.md)
  
[Installieren des Offlinestatus-Add-In-Beispiels](installing-the-sample-offline-state-add-in.md)
  
[Informationen zum Offlinestatus-Add-In-Beispiel](about-the-sample-offline-state-add-in.md)
  
[Einrichten eines Offlinestatus-Add-Ins](setting-up-an-offline-state-add-in.md)
  
[Überwachen von Verbindungsstatusänderungen mit einem Offlinestatus-Add-In](monitoring-connection-state-changes-using-an-offline-state-add-in.md)
  
[Trennen eines Offlinestatus-Add-Ins](disconnecting-an-offline-state-add-in.md)

