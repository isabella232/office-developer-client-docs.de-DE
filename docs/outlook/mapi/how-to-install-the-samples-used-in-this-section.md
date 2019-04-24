---
title: Installieren der in diesem Abschnitt verwendeten Beispiele
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 810f54bf-5b78-46b8-a617-4f61ff816400
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 288ece7a26fb89fa240339da681f163909124823
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345549"
---
# <a name="install-the-samples-used-in-this-section"></a>Installieren der in diesem Abschnitt verwendeten Beispiele

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Führen Sie die folgenden Schritte aus, um die MFCMAPI-Anwendung und das CreateOutlookItemsAddin-Projekt zum Anzeigen und Ausführen des Beispielcodes zu installieren, auf den in den Themen im Abschnitt [Erstellen von Outlook-Elementen mithilfe von MAPI](creating-outlook-items-by-using-mapi.md) verwiesen wird. 

Führen Sie die folgenden Schritte aus, um die im Abschnitt "Verwenden von MAPI zum Erstellen von Outlook-Elementen" verwendeten Beispiele herunterzuladen und zu installieren.

### <a name="to-download-and-install-the-mfcmapi-application-and-open-createoutlookitemsaddin-project"></a>So können Sie die MFCMAPI-Anwendung herunterladen und installieren und das CreateOutlookItemsAddin-Projekt öffnen

1. Laden Sie die aktuelle Version der ausführbaren Datei [MfcMapi](https://go.microsoft.com/fwlink/?LinkID=124154) in einen Ordner auf Ihrem System herunter. 
    
2. Extrahieren Sie die Datei MFCMapi. exe in MFCMapi. exe. _Version_. zip in einen leeren Ordner auf der Festplatte.
    
3. Laden Sie die aktuelle Version des [CreateOutlookItemsAddin](https://go.microsoft.com/fwlink/?LinkID=127828) -Projekts herunter. 
    
4. Extrahieren Sie alle Dateien in der Datei CreateOutlookItemsAddin. zip in den Ordner, in den Sie die Datei MFCMapi. exe in Schritt 2 extrahiert haben.
    
5. Kopieren Sie MFCMapi. exe aus dem in Schritt 2 verwendeten Ordner in das Erstellungsverzeichnis für das CreateOutlookItemsAddin-Projekt (\CreateOutlookItemsAddin\Debug).
    
6. Öffnen Sie das CreateOutlookItemsAddin-Projekt (\CreateOutlookItemsAddin\CreateOutlookItemsAddin.vcproj) in Visual Studio, um den Quellcode zu untersuchen. Informationen zu den zu öffnenden Quelldateien finden Sie in den Themen im Abschnitt [Erstellen von Outlook-Elementen mithilfe von MAPI](creating-outlook-items-by-using-mapi.md) . 
    
## <a name="run-mfcmapi-and-the-createoutlookitemsaddin-project"></a>Ausführen von MFCMAPI und des CreateOutlookItemsAddin-Projekts

Bei den folgenden Schritten wird davon ausgegangen, dass Sie die aktuelle Version der ausführbaren Datei MFCMAPI und das CreateOutlookItemsAddin-Projekt, wie im vorherigen Verfahren beschrieben, heruntergeladen und installiert haben. Diese Schritte führen Sie zu den Menü **** Elementen AddIns, mit denen Sie Outlook-Elemente mithilfe der MfcMapi-Anwendung und des CreateOutlookItemsAddin-Projekts erstellen können. 
  
> [!NOTE]
> Der in Schritt 8 ausgewählte Ordner und der in Schritt 9 ausgewählte Befehl hängen vom Elementtyp ab, der in einem der Themen aus dem Abschnitt [Erstellen von Outlook-Elementen mithilfe von MAPI](creating-outlook-items-by-using-mapi.md) erläutert wird. 

### <a name="to-run-the-mfcmapi-application-and-addins-menu-commands"></a>So führen Sie die Menübefehle MFCMAPI-Anwendung und AddIns aus

1. Starten Sie MfcMapi. exe im Ordner CreateOutlookItemsAddin\Debug, der erstellt wird, wenn Sie die Installationsanweisungen befolgen.
    
2. Klicken Sie auf **OK** , um den Begrüßungsbildschirm von MfcMapi zu schließen. 
    
3. Klicken Sie im Menü **Sitzung** auf **Anmelde-und Anzeige Speichertabelle**.
    
4. Wählen Sie im Dialogfeld **Profil auswählen** das richtige Profil aus, und klicken Sie dann auf **OK**. 
    
5. Doppelklicken Sie in der Listenansicht der Informationsspeichertabelle auf **Postfach- _[Benutzer Name]_ ** . 
    
6. Erweitern Sie in der Ordnerstrukturansicht den Stammknoten. Der Name, der für den Stammknoten angezeigt wird, variiert je nach Typ des ausgewählten Profils. In der Regel wird dieser Knoten als **Stamm Postfach**angezeigt.
    
7. Erweitern Sie in der Ordnerstrukturansicht den Knoten, der den Informationsspeicher enthält. Der für diesen Knoten angezeigte Name variiert je nach Typ des ausgewählten Profils. In der Regel wird dieser Knoten als **IPM_Subtree** oder **Top of Information Store**angezeigt.
    
8. Doppelklicken Sie auf den Ordner für den zu erstellenden Elementtyp. Wenn Sie beispielsweise einen Termin erstellen möchten, klicken Sie auf den Ordner **Termine** . 
    
9. Klicken Sie **** im Menü AddIns auf den entsprechenden Befehl für das zu erstellende Element. 
    
## <a name="download-and-view-code-from-the-mfcmapi-application"></a>Herunterladen und Anzeigen von Code aus der MFCMAPI-Anwendung

Einige Themen beziehen sich auf den Quellcode aus der MFCMAPI-Anwendung selbst. In den folgenden Schritten wird beschrieben, wie Sie den MFCMAPI-Quellcode herunterladen und in Visual Studio anzeigen. 

### <a name="to-download-and-view-the-mfcmapi-application-source-code"></a>So können Sie den Quellcode der MFCMAPI-Anwendung herunterladen und anzeigen

1. Laden Sie den Quellcode für die aktuelle Version der [MfcMapi](https://go.microsoft.com/fwlink/?LinkID=124154) -Anwendung in einen Ordner auf Ihrem System herunter. 
    
2. Extrahieren Sie die Dateien in MFCMAPI __-Changeset. zip in einen leeren Ordner auf Ihrer Festplatte.
    
3. Öffnen Sie das MFCMapi-Projekt __(\ FolderName \ MFCMapi. vcproj) in Visual Studio, um den Quellcode zu untersuchen.
    
## <a name="see-also"></a>Siehe auch

- [Erstellen eines einfachen e-Mail-Elements](how-to-create-a-simple-mail-item.md)
- [Erstellen eines einfachen wiederkehrenden Aufgabenelements](how-to-create-a-simple-recurrent-task-item.md)
- [Erstellen eines komplexen wiederkehrenden Terminelements](how-to-create-a-complex-recurrent-appointment-item.md)
- [Lesen und Analysieren eines Serienmusters](how-to-read-and-parse-a-recurrence-pattern.md)

