---
title: Installieren des eingeWickelten Beispiel-PST-Speicheranbieters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 90ce0ea3-ba73-cb57-0fa9-8898bc4ac9de
description: 'Letzte �nderung: Donnerstag, 5. Juli 2012'
ms.openlocfilehash: a1574de555eb74d06c4dbe721e7e013ac59d3071
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309632"
---
# <a name="installing-the-sample-wrapped-pst-store-provider"></a>Installieren des eingeWickelten Beispiel-PST-Speicheranbieters

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
In diesem Thema werden die Schritte zum herunterladen und Installieren des Beispiels eingeWickelten PST-Speicheranbieters beschrieben. Der beispielhafte PST-Speicheranbieter WrapPST implementiert einen eingebundenen PST-Speicheranbieter, der in Verbindung mit der Replikations-API verwendet werden soll. Weitere Informationen zur Replikations-API finden Sie unter Informationen zur [Replikations-API](about-the-replication-api.md).
  
## <a name="install-the-sample-wrapped-pst-store-provider"></a>Installieren des eingeWickelten Beispiel-PST-Speicheranbieters

1. Informationen zum Herunterladen des eingeWickelten Beispiel-PST-Speicheranbieters finden Sie unter [Outlook 2007 Auxiliary Reference Code Samples and redistributAble Installer](https://www.microsoft.com/en-us/download/details.aspx?id=24102).
    
2. Öffnen Sie den Ordner **SampleWrappedPSTStoreProvider** , und klicken Sie auf **alle Dateien extrahieren**.
    
3. Klicken Sie auf **Durchsuchen**, wählen Sie den Speicherort aus, an dem Sie das Beispiel speichern möchten, und klicken Sie auf **OK**.
    
4. Klicken Sie auf **Extrahieren**. Der ausgewählte Ordner wird angezeigt und enthält die extrahierten Dateien.
    
5. Öffnen Sie Visual Studio 2005 als Administrator.
    
    > [!NOTE]
    > Wenn auf Ihrem Computer Windows XP läuft, müssen Sie als Administrator angemeldet sein. Wenn auf Ihrem Computer Windows Vista ausgeführt wird, müssen Sie als Administrator angemeldet sein, und Sie müssen mit der rechten Maustaste auf das Visual Studio 2005-Symbol klicken und dann **als Administrator ausführen**klicken. 
  
6. Klicken Sie in Visual Studio 2005 auf **Datei**, wählen Sie **Öffnen**aus, und klicken Sie dann auf **Projekt/Lösung**.
    
7. Navigieren Sie zu dem Speicherort, an dem Sie das Beispiel gespeichert haben, klicken Sie auf **WrapPST**, und klicken Sie dann auf **Öffnen**.
    
8. On the **Build** menu, click **Build Solution**.
    
9. Klicken Sie im Dialogfeld **Datei speichern** unter auf **Speichern**.
    
10. Klicken Sie in dem Ordner, in dem Sie das Beispiel gespeichert haben, mit der rechten Maustaste auf die Datei **install. bat** , und klicken Sie dann auf **als Administrator ausführen**.
    
11. Klicken Sie im Dialogfeld **Benutzerkontensteuerung** auf **Weiter**.
    
## <a name="see-also"></a>Siehe auch



[Informationen zum einGebundenen PST-Speicheranbieter](about-the-sample-wrapped-pst-store-provider.md)
  
[Initialisieren eines einGebundenen PST-Speicheranbieters](initializing-a-wrapped-pst-store-provider.md)
  
[Anmelden bei einem einGebundenen PST-Speicheranbieter](logging-on-to-a-wrapped-pst-store-provider.md)
  
[Verwenden eines einGebundenen PST-Speicheranbieters](using-a-wrapped-pst-store-provider.md)
  
[Herunterfahren eines einGebundenen PST-Speicheranbieters](shutting-down-a-wrapped-pst-store-provider.md)

