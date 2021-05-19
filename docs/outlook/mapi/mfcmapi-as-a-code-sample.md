---
title: MFCMAPI als ein Codebeispiel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f98eb842-fe76-4f60-b5e2-d2217d1a66ad
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d72c224db8b3ae4bb6fee3d34f73d9949cda6b8d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356861"
---
# <a name="mfcmapi-as-a-code-sample"></a>MFCMAPI als ein Codebeispiel
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Das MFCMAPI-Beispiel verwendet die Messaging-API, um über eine grafische Benutzeroberfläche Zugriff auf MAPI-Speicher zu ermöglichen. Nachdem Sie dieses Beispiel heruntergeladen haben, können Sie die Quelldateien verwenden, um Beispielverwendungsfälle für viele der MAPI-Schnittstellen und -Verweise zu untersuchen. Weitere Informationen finden Sie unter [MAPI Interfaces](mapi-interfaces.md).
  
|||
|:-----|:-----|
|Plattformen:  <br/> |Microsoft Visual Studio 2008 zum Kompilieren für Windows 7, Windows Vista, Windows Server 2008, Windows XP SP2 und Windows Server 2003 SP1  <br/> |
   
### <a name="to-download-mfcmapi"></a>So laden Sie MFCMAPI herunter
  
1. Klicken Sie auf der [Seite MFCMAPI](https://codeplex.com/MFCMAPI) auf die **Registerkarte Quellcode.** 
    
2. Klicken **Sie unter Zuletztgeprüfte Einchecken** auf **Herunterladen** für den neuesten Build. 
    
3. Lesen Sie den Lizenzvertrag, und klicken Sie dann auf **Ich stimme zu.**
    
4. Klicken Sie im Dialogfeld **Dateidownload** auf **Speichern**. Suchen Sie im Dialogfeld Speichern **unter** den Ordner, in dem Sie die Quelldateien speichern möchten, und klicken Sie dann auf **Speichern**.
    
5. Klicken Sie im Dialogfeld **Download abgeschlossen** auf **Ordner öffnen.** Sie können auch auf **Schließen** klicken, um das Dialogfeld zu schließen und die gezippten Quelldateien in dem Ordner zu finden, in dem Sie sie gespeichert haben. 
    
6. Klicken Sie mit der rechten Maustaste auf die **MFCMAPI-Versionsnummer \< \>.zip** Datei, und klicken Sie dann **auf Alle extrahieren.** Klicken Sie im angezeigten  Dialogfeld auf Extrahieren, um die Dateien in den angezeigten Ordner zu extrahieren. Sie können auch auf **Durchsuchen klicken,** um einen anderen Ordner auszuwählen oder zu erstellen. 
    
7. Führen Visual Studio 2008 als Administrator aus.
    
   > [!NOTE]
   > Wenn Ihr Computer mit Windows XP ausgeführt wird, müssen Sie als Administrator angemeldet sein. Wenn Ihr Computer Windows Vista ausgeführt wird, müssen Sie als Administrator angemeldet sein, und Sie müssen mit der rechten Maustaste auf das Symbol Visual Studio 2008 klicken und dann auf Als Administrator ausführen **klicken.** 
  
8. Klicken Visual Studio 2008 auf **Datei**, zeigen Sie auf **Öffnen** und dann **auf Project/Lösung**.
    
9. Navigieren Sie zu dem Speicherort, an dem Sie das Beispiel gespeichert haben, wählen **Sie MFCMapi.vcproj** aus, und klicken Sie dann auf **Öffnen**.
    
10. On the **Build** menu, click **Build Solution**.
    
11. Klicken Sie im Dialogfeld Datei speichern **unter** auf **Speichern**.
    
### <a name="to-use-mfcmapi-as-a-code-sample"></a>So verwenden Sie MFCMAPI als Codebeispiel
  
Erweitern **Sie im** Projektmappen-Explorer das **MFCMapi-Projekt,** und untersuchen Sie die Dateien in den Knoten **Headerdateien,** **Ressourcendateien** und **Quelldateien** auf Programmierszenarien. 
  
Viele Methodenthemen im Abschnitt [MAPI-Schnittstellen](mapi-interfaces.md) verweisen für Programmierbeispiele auf MFCMAPI-Quelldateien. Beispielsweise werden Sie in [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) angewiesen, die Funktion in der  `CMsgStoreDlg::OnDisplayReceiveFolderTable` Datei MsgStoreDlg.cpp zu betrachten. 
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Beispiele](mapi-samples.md)

