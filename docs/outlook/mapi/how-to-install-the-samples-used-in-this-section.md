---
title: Installieren der in diesem Abschnitt verwendeten Beispiele
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 810f54bf-5b78-46b8-a617-4f61ff816400
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a0ef67ce46c2751f9c38cb6091f8eb1b21108a3e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564309"
---
# <a name="install-the-samples-used-in-this-section"></a>Installieren der in diesem Abschnitt verwendeten Beispiele

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Führen Sie die folgenden Schritte aus, um die MFCMAPI-Anwendung und das CreateOutlookItemsAddin-Projekt zum Anzeigen und Ausführen des Beispielcodes zu installieren, auf den in den Themen im Abschnitt ["Erstellen Outlook Elemente mithilfe von MAPI"](creating-outlook-items-by-using-mapi.md) verwiesen wird. 

Führen Sie die folgenden Schritte aus, um die Im Abschnitt "Verwenden von MAPI zum Erstellen Outlook Elemente" verwendeten Beispiele herunterzuladen und zu installieren.

### <a name="to-download-and-install-the-mfcmapi-application-and-open-createoutlookitemsaddin-project"></a>So laden Sie die MFCMAPI-Anwendung herunter und installieren sie, und öffnen Sie das Projekt "CreateOutlookItemsAddin"

1. Laden Sie die aktuelle Version der ausführbaren [MFCMAPI-Datei](https://go.microsoft.com/fwlink/?LinkID=124154) in einen Ordner auf Ihrem System herunter. 
    
2. Extrahieren Sie die MFCMapi.exe-Datei in MFCMapi.exe. _Version_.zip in einen leeren Ordner auf Der Festplatte.
    
3. Laden Sie die aktuelle Version des [Projekts CreateOutlookItemsAddin](https://go.microsoft.com/fwlink/?LinkID=127828) herunter. 
    
4. Extrahieren Sie alle Dateien in der CreateOutlookItemsAddin.zip-Datei in den Ordner, in den Sie die MFCMapi.exe-Datei in Schritt 2 extrahiert haben.
    
5. Kopieren Sie MFCMapi.exe aus dem in Schritt 2 verwendeten Ordner in das Buildverzeichnis für das CreateOutlookItemsAddin-Projekt (\CreateOutlookItemsAddin\Debug).
    
6. Öffnen Sie das Projekt CreateOutlookItemsAddin (\CreateOutlookItemsAddin\CreateOutlookItemsAddin.vcproj) in Visual Studio, um den Quellcode zu untersuchen. Lesen Sie die Themen aus dem Abschnitt ["Erstellen von Outlook Elementen mithilfe von MAPI",](creating-outlook-items-by-using-mapi.md) um zu bestimmen, welche Quelldateien geöffnet werden sollen. 
    
## <a name="run-mfcmapi-and-the-createoutlookitemsaddin-project"></a>Ausführen von MFCMAPI und des Projekts "CreateOutlookItemsAddin"

Bei den folgenden Schritten wird davon ausgegangen, dass Sie die aktuelle Version der ausführbaren MFCMAPI-Datei und des Projekts CreateOutlookItemsAddin wie im vorherigen Verfahren beschrieben heruntergeladen und installiert haben. Diese Schritte führen Sie zu den **Addins-Menüelementen,** mit denen Sie Outlook Elemente mit der MFCMAPI-Anwendung und dem CreateOutlookItemsAddin-Projekt erstellen können. 
  
> [!NOTE]
> Der Ordner, den Sie in Schritt 8 auswählen, und der Befehl, den Sie in Schritt 9 auswählen, hängt vom Elementtyp ab, der in einem der Themen aus dem Abschnitt ["Erstellen Outlook Elemente mithilfe von MAPI"](creating-outlook-items-by-using-mapi.md) erläutert wird. 

### <a name="to-run-the-mfcmapi-application-and-addins-menu-commands"></a>So führen Sie die Menübefehle der MFCMAPI-Anwendung und der Add-Ins aus

1. Starten Sie Mfcmapi.exe im Ordner "CreateOutlookItemsAddin\Debug", der erstellt wird, wenn Sie die Installationsanweisungen befolgen.
    
2. Klicken Sie auf **"OK",** um den MFCMAPI-Begrüßungsbildschirm zu schließen. 
    
3. Klicken Sie im Menü **"Sitzung"** auf **"Anmelden" und "Store Tabelle anzeigen".**
    
4. Wählen **Sie** im Dialogfeld Profil auswählen das richtige Profil aus, und klicken Sie dann auf **OK.** 
    
5. Doppelklicken Sie auf **"Postfach" _– [Benutzername]_** in der Listenansicht der Speichertabelle. 
    
6. Erweitern Sie in der Ordnerstrukturansicht den Stammknoten. Der für den Stammknoten angezeigte Name hängt vom ausgewählten Profiltyp ab. In der Regel wird dieser Knoten als Stamm - **Postfach** angezeigt.
    
7. Erweitern Sie in der Ordnerstrukturansicht den Knoten, der den Informationsspeicher enthält. Der für diesen Knoten angezeigte Name hängt vom ausgewählten Profiltyp ab. In der Regel wird dieser Knoten als **IPM_SUBTREE** oder **oben Store** angezeigt.
    
8. Doppelklicken Sie auf den Ordner für den zu erstellenden Elementtyp. Wenn Sie beispielsweise einen Termin erstellen möchten, klicken Sie auf den Ordner **"Termine".** 
    
9. Klicken Sie im **Menü "Addins"** auf den entsprechenden Befehl für das zu erstellende Element. 
    
## <a name="download-and-view-code-from-the-mfcmapi-application"></a>Herunterladen und Anzeigen von Code aus der MFCMAPI-Anwendung

Einige Themen beziehen sich auf Quellcode aus der MFCMAPI-Anwendung selbst. In den folgenden Schritten wird beschrieben, wie Sie den MFCMAPI-Quellcode herunterladen und in Visual Studio anzeigen. 

### <a name="to-download-and-view-the-mfcmapi-application-source-code"></a>So laden Sie den Quellcode der MFCMAPI-Anwendung herunter und zeigen diesen an

1. Laden Sie den Quellcode für die aktuelle Version der [MFCMAPI-Anwendung](https://go.microsoft.com/fwlink/?LinkID=124154) in einen Ordner auf Ihrem System herunter. 
    
2. Extrahieren Sie die Dateien in MFCMAPI- _changeset_.zip in einen leeren Ordner auf Ihrer Festplatte.
    
3. Öffnen Sie das MFCMapi-Projekt (\ _Ordnername_\ MFCMapi.vcproj) in Visual Studio, um den Quellcode zu untersuchen.
    
## <a name="see-also"></a>Siehe auch

- [Erstellen eines einfachen E-Mail-Elements](how-to-create-a-simple-mail-item.md)
- [Erstellen eines einfachen wiederkehrenden Aufgabenelements](how-to-create-a-simple-recurrent-task-item.md)
- [Erstellen eines komplexen Terminserienelements](how-to-create-a-complex-recurrent-appointment-item.md)
- [Lesen und Analysieren eines Serienmusters](how-to-read-and-parse-a-recurrence-pattern.md)

