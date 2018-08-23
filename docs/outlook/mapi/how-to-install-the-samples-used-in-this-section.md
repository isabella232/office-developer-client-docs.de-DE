---
title: Installieren Sie die Beispiele in diesem Abschnitt
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 810f54bf-5b78-46b8-a617-4f61ff816400
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 0b4cc2fe82db60a2302f33a194314e0df1458a89
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586914"
---
# <a name="install-the-samples-used-in-this-section"></a>Installieren Sie die Beispiele in diesem Abschnitt

**Betrifft**: Outlook 2013 | Outlook 2016 
  
Gehen Sie folgendermaßen vor, um MFCMAPI (engl.) Anwendung und CreateOutlookItemsAddin Projekt anzeigen, und führen Sie den Beispielcode, die durch die Themen im Abschnitt [Erstellen von Outlook-Elementen mithilfe von MAPI](creating-outlook-items-by-using-mapi.md) zu installieren. 

Herunterladen und installieren die Beispielen in "Using MAPI zum Erstellen von Outlook-Elemente" im Abschnitt, gehen Sie folgendermaßen vor.

### <a name="to-download-and-install-the-mfcmapi-application-and-open-createoutlookitemsaddin-project"></a>Herunterladen und installieren Sie die Anwendung MFCMAPI (engl.) und CreateOutlookItemsAddin Projekt öffnen

1. Laden Sie die aktuelle Version der ausführbaren [MFCMAPI (engl.)](http://go.microsoft.com/fwlink/?LinkID=124154) , in einen Ordner auf Ihrem System. 
    
2. Extrahieren Sie die Datei MFCMapi.exe in MFCMapi.exe. _Version_ZIP in einen leeren Ordner auf Ihrer Festplatte.
    
3. Laden Sie die aktuelle Version des Projekts [CreateOutlookItemsAddin](http://go.microsoft.com/fwlink/?LinkID=127828) . 
    
4. Extrahieren Sie alle Dateien in der Datei CreateOutlookItemsAddin.zip in den Ordner, in dem Sie die Datei MFCMapi.exe in Schritt2 extrahiert haben.
    
5. Kopieren Sie MFCMapi.exe aus dem Ordner, der in Schritt2 auf das Buildverzeichnis für das Projekt CreateOutlookItemsAddin (\CreateOutlookItemsAddin\Debug) verwendet.
    
6. Öffnen Sie das Projekt CreateOutlookItemsAddin (\CreateOutlookItemsAddin\CreateOutlookItemsAddin.vcproj) in Visual Studio den Quellcode untersuchen. Finden Sie in den Themen aus dem Abschnitt [Erstellen von Outlook-Elementen mithilfe von MAPI](creating-outlook-items-by-using-mapi.md) zu ermitteln, welcher Quelle Dateien um zu öffnen. 
    
## <a name="run-mfcmapi-and-the-createoutlookitemsaddin-project"></a>Führen Sie MFCMAPI (engl.) und das CreateOutlookItemsAddin-Projekt

Die folgenden Schritte wird davon ausgegangen, dass Sie heruntergeladen und die aktuelle Version der ausführbaren Datei MFCMAPI (engl.) und das Projekt CreateOutlookItemsAddin installiert wie im vorherigen Verfahren beschrieben. Diese Schritte bieten Ihnen an die Menüelemente **-Add-Ins** Anleitungen, mit die Sie Outlook-Elemente mithilfe der Anwendung MFCMAPI (engl.) und das Projekt CreateOutlookItemsAddin erstellen können. 
  
> [!NOTE]
> Der Ordner, den Sie in Schritt 8 und den Befehl, den Sie in Schritt 9, wählen Sie auswählen, hängt von den Elementtyp in den Themen im Abschnitt [Erstellen von Outlook-Elementen mithilfe von MAPI](creating-outlook-items-by-using-mapi.md) erläuterten ab. 

### <a name="to-run-the-mfcmapi-application-and-addins-menu-commands"></a>Zum Ausführen der Anwendung MFCMAPI (engl.) und Menübefehle-Add-Ins

1. Starten Sie Mfcmapi.exe im Ordner "CreateOutlookItemsAddin\Debug", die erstellt wird, wenn Sie die installationsanweisungen folgen.
    
2. Klicken Sie auf **OK** , um den Begrüßungsbildschirm MFCMAPI (engl.) zu schließen. 
    
3. Klicken Sie im Menü **Sitzung** auf **Anmelde- und zeigt die Tabelle Store**.
    
4. Klicken Sie im Dialogfeld **Profil auswählen** wählen Sie das richtige Profil aus, und klicken Sie dann auf **OK**. 
    
5. Doppelklicken Sie in der Listenansicht des Store-Tabelle auf **Postfach – _[Benutzername]_ ** . 
    
6. Erweitern Sie in der Strukturansicht des Ordners den Stammknoten aus. Der Name für den Stammknoten angezeigt variiert je nach den Typ des Profils ausgewählt. Dieser Knoten wird in der Regel als **Stamm - Postfach**angezeigt.
    
7. Erweitern Sie in der Strukturansicht des Ordners den Knoten, der den Informationsspeicher enthält. Der Name für diesen Knoten angezeigt variiert je nach den Typ des Profils ausgewählt. Dieser Knoten wird in der Regel als **IPM_SUBTREE** oder die **Oberste Ebene des Informationsspeichers**angezeigt.
    
8. Doppelklicken Sie auf den Ordner für den jeweiligen Elementtyp zu erstellen. Klicken Sie auf den Ordner **Termine** beispielsweise zum Erstellen eines Termins. 
    
9. Klicken Sie im Menü **-Add-Ins** auf den entsprechenden Befehl für das Element zu erstellen. 
    
## <a name="download-and-view-code-from-the-mfcmapi-application"></a>Herunterladen und Anzeigen von Code aus der Anwendung MFCMAPI (engl.)

Einige Themen verweisen auf Quellcode aus der MFCMAPI (engl.)-Anwendung selbst. Die folgenden Schritte beschreiben, wie Sie den Quellcode MFCMAPI (engl.) herunter und zeigen Sie es in Visual Studio. 

### <a name="to-download-and-view-the-mfcmapi-application-source-code"></a>Herunterladen und anzeigen den Anwendungsquellcode MFCMAPI (engl.)

1. Laden Sie den Quellcode für die aktuelle Version der Anwendung in einen Ordner auf Ihrem System [MFCMAPI (engl.)](http://go.microsoft.com/fwlink/?LinkID=124154) . 
    
2. Extrahieren Sie die Dateien in MFCMAPI (engl.) - _Changeset_ZIP in einen leeren Ordner auf Ihrer Festplatte.
    
3. Öffnen Sie das Projekt MFCMAPI (engl.) (\ _Foldername_\ MFCMapi.vcproj) in Visual Studio, um den Quellcode zu überprüfen.
    
## <a name="see-also"></a>Siehe auch

- [Erstellen eines einfachen E-Mail-Elements](how-to-create-a-simple-mail-item.md)
- [Erstellen eines einfachen wiederkehrenden Aufgabenelements](how-to-create-a-simple-recurrent-task-item.md)
- [Erstellen eines komplexen Terminserienelements](how-to-create-a-complex-recurrent-appointment-item.md)
- [Lesen und Analysieren eines Serienmusters](how-to-read-and-parse-a-recurrence-pattern.md)

