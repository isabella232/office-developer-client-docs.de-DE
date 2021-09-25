---
title: MFCMAPI als ein Codebeispiel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: f98eb842-fe76-4f60-b5e2-d2217d1a66ad
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e3cd4a473d38b2a006602ad21a9dca0de0df4e85
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59613667"
---
# <a name="mfcmapi-as-a-code-sample"></a>MFCMAPI als ein Codebeispiel
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Im MFCMAPI-Beispiel wird die Messaging-API verwendet, um den Zugriff auf MAPI-Speicher über eine grafische Benutzeroberfläche zu ermöglichen. Nachdem Sie dieses Beispiel heruntergeladen haben, können Sie die Quelldateien verwenden, um Beispielanwendungsfälle für viele der MAPI-Schnittstellen und -Verweise zu untersuchen. Weitere Informationen finden Sie unter [MAPI-Schnittstellen.](mapi-interfaces.md)
  
|||
|:-----|:-----|
|Plattformen:  <br/> |Microsoft Visual Studio 2008 zum Kompilieren für Windows 7, Windows Vista, Windows Server 2008, Windows XP SP2 und Windows Server 2003 SP1  <br/> |
   
### <a name="to-download-mfcmapi"></a>So laden Sie MFCMAPI herunter
  
1. Klicken Sie auf der [MFCMAPI-Seite](https://codeplex.com/MFCMAPI) auf die Registerkarte **"Quellcode".** 
    
2. Klicken Sie unter **"Zuletzt verwendete Eincheckvorgänge"** auf **"Herunterladen"** für den neuesten Build. 
    
3. Lesen Sie den Lizenzvertrag, und klicken Sie dann auf **"Ich stimme zu".**
    
4. Klicken Sie im Dialogfeld **Dateidownload** auf **Speichern**. Suchen Sie im Dialogfeld Speichern **unter** den Ordner, in dem Sie die Quelldateien speichern möchten, und klicken Sie dann auf **"Speichern".**
    
5. Klicken Sie im Dialogfeld **"Vollständig herunterladen"** auf **"Ordner öffnen".** Sie können auch auf **"Schließen"** klicken, um das Dialogfeld zu schließen und die gezippten Quelldateien in dem Ordner zu suchen, in dem Sie sie gespeichert haben. 
    
6. Klicken Sie mit der rechten Maustaste auf die **Datei MFCMAPI- \<version number\>.zip,** und klicken Sie dann auf **"Alle extrahieren".** Klicken Sie im daraufhin angezeigten Dialogfeld auf **"Extrahieren",** um die Dateien in den angezeigten Ordner zu extrahieren. Sie können auch auf **"Durchsuchen"** klicken, um einen anderen Ordner auszuwählen oder zu erstellen. 
    
7. Führen Sie Visual Studio 2008 als Administrator aus.
    
   > [!NOTE]
   > Wenn Ihr Computer Windows XP ausgeführt wird, müssen Sie als Administrator angemeldet sein. Wenn Ihr Computer Windows Vista ausgeführt wird, müssen Sie als Administrator angemeldet sein, und Sie müssen mit der rechten Maustaste auf das Symbol Visual Studio 2008 klicken und dann **auf "Als Administrator ausführen"** klicken. 
  
8. Klicken Sie in Visual Studio 2008 auf **"Datei",** zeigen Sie auf **"Öffnen",** und klicken Sie dann auf **Project/Lösung.**
    
9. Navigieren Sie zu dem Speicherort, an dem Sie das Beispiel gespeichert haben, wählen Sie **"MFCMapi.vcproj"** aus, und klicken Sie dann auf **"Öffnen".**
    
10. On the **Build** menu, click **Build Solution**.
    
11. Klicken Sie im Dialogfeld **"Datei speichern unter"** auf **"Speichern".**
    
### <a name="to-use-mfcmapi-as-a-code-sample"></a>So verwenden Sie MFCMAPI als Codebeispiel
  
Erweitern Sie im **Projektmappen-Explorer** das **MFCMapi-Projekt,** und untersuchen Sie die Dateien in den Knoten **"Headerdateien",** **"Ressourcendateien"** und **"Quelldateien"** für Programmierszenarien. 
  
Viele Methodenthemen im Abschnitt [MAPI-Schnittstellen](mapi-interfaces.md) verweisen auf MFCMAPI-Quelldateien für Programmierbeispiele. In [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) werden Sie beispielsweise angewiesen, sich die Funktion  `CMsgStoreDlg::OnDisplayReceiveFolderTable` in der Datei "MsgStoreDlg.cpp" anzusehen. 
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Beispiele](mapi-samples.md)

