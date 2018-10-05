---
title: MFCMAPI (engl.) als ein Codebeispiel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f98eb842-fe76-4f60-b5e2-d2217d1a66ad
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d72c224db8b3ae4bb6fee3d34f73d9949cda6b8d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391661"
---
# <a name="mfcmapi-as-a-code-sample"></a>MFCMAPI (engl.) als ein Codebeispiel
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Das MFCMAPI (engl.) Beispiel verwendet der Messaging-API, Zugriff auf MAPI-Speicher über eine grafische Benutzeroberfläche ermöglicht. Nachdem Sie dieses Beispiel herunterladen, können Sie die Quelldateien, um Beispiel Usage Fälle für viele der MAPI-Schnittstellen und Verweise zu überprüfen. Weitere Informationen finden Sie unter [MAPI-Schnittstellen](mapi-interfaces.md).
  
|||
|:-----|:-----|
|Plattformen:  <br/> |Microsoft Visual Studio 2008 zum Kompilieren für Windows 7, Windows Vista, Windows Server 2008, Windows XP SP2 und Windows Server 2003 SP1  <br/> |
   
### <a name="to-download-mfcmapi"></a>MFCMAPI (engl.) herunterladen
  
1. Klicken Sie auf der Seite [MFCMAPI (engl.)](https://codeplex.com/MFCMAPI) auf der Registerkarte **Quellcode** . 
    
2. Klicken Sie unter **Zuletzt verwendete Eincheckvorgänge**auf **Download** für den aktuellen Build. 
    
3. Lesen Sie den Lizenzvertrag, und klicken Sie dann auf **ich stimme zu**.
    
4. Klicken Sie im Dialogfeld **Dateidownload** auf **Speichern**. Klicken Sie im Dialogfeld **Speichern unter** Suchen nach dem Ordner, in dem Sie die Quelldateien speichern möchten, und klicken Sie dann auf **Speichern**.
    
5. Klicken Sie im Dialogfeld **Download abgeschlossen** auf **Ordner öffnen**. Sie können auch klicken Sie auf **Schließen** , um das Dialogfeld zu schließen, und suchen die ZIP-Quelldateien in dem Ordner, dem Sie sie gespeichert haben. 
    
6. Mit der rechten Maustaste die **MFCMAPI (engl.) -\<Versionsnummer\>ZIP** Datei, und klicken Sie dann auf **Alle extrahieren**. Klicken Sie im Dialogfeld, das angezeigt wird, klicken Sie auf **extrahieren** , zum Extrahieren der Dateien in den Ordner, der angezeigt wird. Sie können auch klicken Sie auf **Durchsuchen** , um wählen oder erstellen Sie einen anderen Ordner. 
    
7. Visual Studio 2008 als Administrator ausführen.
    
   > [!NOTE]
   > Wenn Ihr Computer unter Windows XP ausgeführt wird, müssen Sie als Administrator angemeldet sein,. Wenn Ihr Computer Windows Vista ausgeführt wird, Sie müssen als Administrator angemeldet sein, und Sie mit der rechten Maustaste in des Visual Studio 2008-Symbols und klicken Sie dann auf **als Administrator ausführen**müssen. 
  
8. Klicken Sie in Visual Studio 2008 auf **Datei**, zeigen Sie auf **Öffnen**, und klicken Sie dann auf **Projekt/Projektmappe**.
    
9. Navigieren Sie zum Speicherort, in dem Sie das Beispiel gespeichert haben, wählen Sie **MFCMapi.vcproj**aus und klicken Sie dann auf **Öffnen**.
    
10. On the **Build** menu, click **Build Solution**.
    
11. Klicken Sie im Dialogfeld **Datei speichern unter** auf **Speichern**.
    
### <a name="to-use-mfcmapi-as-a-code-sample"></a>MFCMAPI (engl.) als ein Codebeispiel verwenden
  
Klicken Sie im **Projektmappen-Explorer**erweitern Sie das Projekt **MFCMAPI (engl.)** , und untersuchen Sie die Dateien in den Knoten **Headerdateien**, **Ressourcendateien**und **Quelldateien** für Programmierung Szenarien. 
  
Viele Themen im Abschnitt [MAPI-Schnittstellen](mapi-interfaces.md) zeigen Sie auf die Quelldateien für Programmierbeispiele MFCMAPI (engl.). Beispielsweise in [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) Sie werden aufgefordert, betrachten die Funktion `CMsgStoreDlg::OnDisplayReceiveFolderTable` in der Datei MsgStoreDlg.cpp. 
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Beispiele](mapi-samples.md)

