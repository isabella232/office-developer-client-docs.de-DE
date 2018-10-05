---
title: Installieren des Beispiel für einen Anbieter von umschlossenem PST-Speicher
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 90ce0ea3-ba73-cb57-0fa9-8898bc4ac9de
description: 'Letzte �nderung: Donnerstag, 5. Juli 2012'
ms.openlocfilehash: a1574de555eb74d06c4dbe721e7e013ac59d3071
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397765"
---
# <a name="installing-the-sample-wrapped-pst-store-provider"></a>Installieren des Beispiel für einen Anbieter von umschlossenem PST-Speicher

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
In diesem Thema führt Sie durch die Schritte zum Herunterladen und Installieren der umbrochen PST Store Beispielanbieter. Die umfließendem PST-Datei speichern Beispielanbieter, WrapPST, implementiert einen gepackten PST-Anbieter, der in Verbindung mit der API für die Replikation verwendet werden soll. Weitere Informationen zur Replikation-API finden Sie unter [Über die Replikation-API](about-the-replication-api.md).
  
## <a name="install-the-sample-wrapped-pst-store-provider"></a>Installieren des Beispielanbieters gepackten PST-Speichers

1. Um die umfließendem PST Store Beispielanbieter herunterladen möchten, finden Sie unter [Outlook 2007: zusätzliche Referenzcodebeispiele und verteilbares Installationsprogramm](https://www.microsoft.com/en-us/download/details.aspx?id=24102).
    
2. Öffnen Sie den Ordner **SampleWrappedPSTStoreProvider** , und klicken Sie auf **Allerdateien extrahieren**.
    
3. Klicken Sie auf **Durchsuchen**, markieren Sie den Speicherort, in dem Sie das Beispiel zu speichern möchten, und klicken Sie auf **OK**.
    
4. Klicken Sie auf **Extract**. Der Ordner gewählte angezeigt wird und die extrahierten Dateien enthält.
    
5. Öffnen Sie Visual Studio 2005 als Administrator an.
    
    > [!NOTE]
    > Wenn Ihr Computer unter Windows XP ausgeführt wird, müssen Sie als Administrator angemeldet sein,. Wenn Ihr Computer Windows Vista ausgeführt wird, müssen Sie als Administrator, und Sie müssen mit der rechten Maustaste in des Visual Studio 2005-Symbols und klicken Sie auf **als Administrator ausführen**angemeldet sein. 
  
6. Klicken Sie in Visual Studio 2005 auf **Datei**, klicken Sie auf **Öffnen**, und klicken Sie dann auf **Projekt/Projektmappe**.
    
7. Navigieren Sie zum Speicherort, in dem Sie das Beispiel gespeichert haben, klicken Sie auf **WrapPST**und klicken Sie dann auf **Öffnen**.
    
8. On the **Build** menu, click **Build Solution**.
    
9. Klicken Sie im Dialogfeld **Datei speichern unter** auf **Speichern**.
    
10. In den Ordner, in dem Sie das Beispiel gespeichert haben, mit der rechten Maustaste in der Datei **Install.bat aus** , und klicken Sie auf **als Administrator ausführen**.
    
11. Klicken Sie im Dialogfeld **Benutzerkontensteuerung** auf **Weiter**.
    
## <a name="see-also"></a>Siehe auch



[Informationen über das Beispiel für einen Anbieter von umschlossenem PST-Speicher](about-the-sample-wrapped-pst-store-provider.md)
  
[Initialisieren eines Anbieters von umschlossenem PST-Speicher](initializing-a-wrapped-pst-store-provider.md)
  
[Anmelden bei einem Anbieter von umschlossenem PST-Speicher](logging-on-to-a-wrapped-pst-store-provider.md)
  
[Verwenden eines Anbieters von umschlossenem PST-Speicher](using-a-wrapped-pst-store-provider.md)
  
[Herunterfahren eines Anbieters von umschlossenem PST-Speicher](shutting-down-a-wrapped-pst-store-provider.md)

