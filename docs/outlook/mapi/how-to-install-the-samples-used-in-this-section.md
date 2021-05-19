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
  
Führen Sie die folgenden Schritte aus, um die MFCMAPI-Anwendung und das CreateOutlookItemsAddin-Projekt zum Anzeigen und Ausführen des Beispielcodes zu installieren, auf den in den Themen im Abschnitt Erstellen von Outlook-Elementen mithilfe von [MAPI](creating-outlook-items-by-using-mapi.md) verwiesen wird. 

Führen Sie die folgenden Schritte aus, um die beispiele herunterzuladen und zu installieren, die im Abschnitt "Verwenden von MAPI zum Erstellen Outlook Elemente" verwendet werden.

### <a name="to-download-and-install-the-mfcmapi-application-and-open-createoutlookitemsaddin-project"></a>So laden Sie die MFCMAPI-Anwendung herunter und installieren sie, und öffnen Sie das CreateOutlookItemsAddin-Projekt

1. Laden Sie die aktuelle Version der [ausführbaren MFCMAPI](https://go.microsoft.com/fwlink/?LinkID=124154) in einen Ordner auf Ihrem System herunter. 
    
2. Extrahieren Sie MFCMapi.exe Datei in MFCMapi.exe. _Version_.zip in einen leeren Ordner auf der Festplatte.
    
3. Laden Sie die aktuelle Version des [CreateOutlookItemsAddin-Projekts](https://go.microsoft.com/fwlink/?LinkID=127828) herunter. 
    
4. Extrahieren Sie alle Dateien in der CreateOutlookItemsAddin.zip in den Ordner, in dem Sie die Datei MFCMapi.exe Schritt 2 extrahiert haben.
    
5. Kopieren MFCMapi.exe aus dem ordner, der in Schritt 2 verwendet wird, in das Buildverzeichnis für das CreateOutlookItemsAddin-Projekt (\CreateOutlookItemsAddin\Debug).
    
6. Öffnen Sie das CreateOutlookItemsAddin-Projekt (\CreateOutlookItemsAddin\CreateOutlookItemsAddin.vcproj) in Visual Studio, um den Quellcode zu untersuchen. Lesen Sie die Themen aus dem Abschnitt Erstellen Outlook Elemente mithilfe von [MAPI,](creating-outlook-items-by-using-mapi.md) um zu bestimmen, welche Quelldateien geöffnet werden. 
    
## <a name="run-mfcmapi-and-the-createoutlookitemsaddin-project"></a>Ausführen von MFCMAPI und dem CreateOutlookItemsAddin-Projekt

In den folgenden Schritten wird davon ausgegangen, dass Sie die aktuelle Version der ausführbaren MFCMAPI und des CreateOutlookItemsAddin-Projekts heruntergeladen und installiert haben, wie im vorherigen Verfahren beschrieben. Diese Schritte führen Sie  zu den Addins-Menüelementen, mit denen Sie mithilfe der MFCMAPI-Anwendung und des CreateOutlookItemsAddin-Projekts Outlook Elemente erstellen können. 
  
> [!NOTE]
> Der ordner, den Sie in Schritt 8 auswählen, und der Befehl, den Sie in Schritt 9 auswählen, hängt vom Elementtyp ab, der in einem der Themen aus dem Abschnitt Erstellen von Outlook Elementen mithilfe von [MAPI](creating-outlook-items-by-using-mapi.md) erläutert wird. 

### <a name="to-run-the-mfcmapi-application-and-addins-menu-commands"></a>So führen Sie die Befehle MFCMAPI-Anwendung und Addins aus

1. Starten Mfcmapi.exe im Ordner CreateOutlookItemsAddin\Debug, der erstellt wird, wenn Sie die Installationsanweisungen befolgen.
    
2. Klicken **Sie auf OK,** um den MFCMAPI-Begrüßungsbildschirm zu schließen. 
    
3. Klicken Sie **im** Menü Sitzung auf **Logon and Display Store Table**.
    
4. Wählen Sie im Dialogfeld **Profil** auswählen das richtige Profil aus, und klicken Sie dann auf **OK**. 
    
5. Doppelklicken Sie in der Listenansicht der Speichertabelle auf Postfach – **_[Benutzername]._** 
    
6. Erweitern Sie in der Ordnerstrukturansicht den Stammknoten. Der für den Stammknoten angezeigte Name variiert je nach ausgewähltem Profiltyp. In der Regel wird dieser Knoten als **Stammpostfach angezeigt.**
    
7. Erweitern Sie in der Ordnerstrukturansicht den Knoten, der den Informationsspeicher enthält. Der für diesen Knoten angezeigte Name variiert je nach ausgewähltem Profiltyp. In der Regel wird  dieser Knoten als IPM_SUBTREE **oder Top of Information Store angezeigt.**
    
8. Doppelklicken Sie auf den Ordner für den zu erstellende Elementtyp. Klicken Sie zum Erstellen eines **Termins** beispielsweise auf den Ordner Termine. 
    
9. Klicken Sie **im Menü Addins** auf den entsprechenden Befehl für das zu erstellende Element. 
    
## <a name="download-and-view-code-from-the-mfcmapi-application"></a>Herunterladen und Anzeigen von Code aus der MFCMAPI-Anwendung

Einige Themen beziehen sich auf Quellcode aus der MFCMAPI-Anwendung selbst. In den folgenden Schritten wird beschrieben, wie Sie den MFCMAPI-Quellcode herunterladen und in einem Visual Studio. 

### <a name="to-download-and-view-the-mfcmapi-application-source-code"></a>So laden Sie den QUELLCODE der MFCMAPI-Anwendung herunter und zeigen diesen an

1. Laden Sie den Quellcode für die aktuelle Version der [MFCMAPI-Anwendung](https://go.microsoft.com/fwlink/?LinkID=124154) in einen Ordner auf Ihrem System herunter. 
    
2. Extrahieren Sie die Dateien in MFCMAPI- _changeset_.zip in einen leeren Ordner auf der Festplatte.
    
3. Öffnen Sie das MFCMapi-Projekt (\ _foldername_\ MFCMapi.vcproj) in Visual Studio, um den Quellcode zu untersuchen.
    
## <a name="see-also"></a>Siehe auch

- [Erstellen eines einfachen E-Mail-Elements](how-to-create-a-simple-mail-item.md)
- [Erstellen eines einfachen Wiederkehrenden Aufgabenelements](how-to-create-a-simple-recurrent-task-item.md)
- [Erstellen eines komplexen Terminelements mit wiederkehrenden Terminen](how-to-create-a-complex-recurrent-appointment-item.md)
- [Lesen und Analysieren eines Serienmusters](how-to-read-and-parse-a-recurrence-pattern.md)

