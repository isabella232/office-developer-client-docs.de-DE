---
title: Installieren des Beispielanbieters für pst-Store
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 90ce0ea3-ba73-cb57-0fa9-8898bc4ac9de
description: 'Letzte �nderung: Donnerstag, 5. Juli 2012'
ms.openlocfilehash: 2b47d2bc38ae0d61bbfb2a4002734b00bbfcbece
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620646"
---
# <a name="installing-the-sample-wrapped-pst-store-provider"></a>Installieren des Beispielanbieters für pst-Store

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
In diesem Thema werden sie durch die Schritte zum Herunterladen und Installieren des Beispielanbieters für pst-Store geführt. Das Beispiel für einen umbrochenen PST-Store-Anbieter, WrapPST, implementiert einen umschlossenen PST-Speicheranbieter, der in Verbindung mit der Replikations-API verwendet werden soll. Weitere Informationen zur Replikations-API finden Sie unter ["Informationen zur Replikations-API".](about-the-replication-api.md)
  
## <a name="install-the-sample-wrapped-pst-store-provider"></a>Installieren des PsT-Beispielanbieters Store

1. Informationen zum Herunterladen des Beispiels für einen umschlossenen PST-Store-Anbieter finden Sie unter [Outlook 2007 Auxiliary Reference Code Samples and Redistributable Installer](https://www.microsoft.com/en-us/download/details.aspx?id=24102).
    
2. Öffnen Sie den Ordner **SampleWrappedPSTStoreProvider,** und klicken Sie auf **"Alle Dateien extrahieren".**
    
3. Klicken Sie auf **"Durchsuchen",** wählen Sie den Speicherort aus, an dem Sie das Beispiel speichern möchten, und klicken Sie auf **"OK".**
    
4. Klicken Sie auf **Extrahieren**. Der ausgewählte Ordner wird angezeigt und enthält die extrahierten Dateien.
    
5. Öffnen Sie Visual Studio 2005 als Administrator.
    
    > [!NOTE]
    > Wenn Ihr Computer Windows XP ausgeführt wird, müssen Sie als Administrator angemeldet sein. Wenn Ihr Computer Windows Vista ausgeführt wird, müssen Sie als Administrator angemeldet sein, und Sie müssen mit der rechten Maustaste auf das Symbol Visual Studio 2005 klicken und **auf "Als Administrator ausführen"** klicken. 
  
6. Klicken Sie in Visual Studio 2005 auf **"Datei",** wählen Sie **"Öffnen"** aus, und klicken Sie dann auf **Project/Projektmappe.**
    
7. Navigieren Sie zu dem Speicherort, an dem Sie das Beispiel gespeichert haben, klicken Sie auf **"WrapPST"** und dann auf **"Öffnen".**
    
8. On the **Build** menu, click **Build Solution**.
    
9. Klicken Sie im Dialogfeld **"Datei speichern unter"** auf **"Speichern".**
    
10. Klicken Sie in dem Ordner, in dem Sie das Beispiel gespeichert haben, mit der rechten Maustaste auf die **dateiInstall.bat,** und klicken Sie auf **"Als Administrator ausführen".**
    
11. Klicken Sie im Dialogfeld **Benutzerkontensteuerung** auf **Weiter**.
    
## <a name="see-also"></a>Siehe auch



[Informationen zum Beispiel für pst-Store-Anbieter mit Umschlossenen](about-the-sample-wrapped-pst-store-provider.md)
  
[Initialisieren eines Anbieters von umschlossenen PST-Store](initializing-a-wrapped-pst-store-provider.md)
  
[Anmelden bei einem anbieter umschlossenen PST-Store](logging-on-to-a-wrapped-pst-store-provider.md)
  
[Verwenden eines Anbieters von umschlossenen PST-Store](using-a-wrapped-pst-store-provider.md)
  
[Herunterfahren eines Anbieters von umschlossenen PST-Store](shutting-down-a-wrapped-pst-store-provider.md)

