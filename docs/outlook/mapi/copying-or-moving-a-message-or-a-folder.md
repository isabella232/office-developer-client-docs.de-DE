---
title: Kopieren oder Verschieben einer Nachricht oder eines Ordners
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 72290fd3-00d7-4055-bbfa-0c47b6e0f62d
description: 'Last modified: November 08, 2011'
ms.openlocfilehash: c06fee83d217339d48d66963a721143c9d26e25b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567732"
---
# <a name="copying-or-moving-a-message-or-a-folder"></a>Kopieren oder Verschieben einer Nachricht oder eines Ordners
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Client kann eine von vier Methoden zum Kopieren oder Verschieben einer Nachricht oder eines Ordners verwenden:
  
- [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md)
    
- [IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
    
- [IMAPIProp::CopyTo](imapiprop-copyto.md)
    
- [IMAPIProp::CopyProps](imapiprop-copyprops.md)
    
Durch Festlegen der entsprechenden Flags und Parameter können **CopyTo** und **CopyProps** genauso wie **CopyFolder** oder **CopyMessages** verwendet werden. Berücksichtigen Sie die folgenden Probleme bei der Entscheidung, welche Methode aufgerufen werden soll:
  
- Kopieren oder verschieben Sie einen Ordner oder eine Nachricht?
    
- Wie viel wissen Sie über den Ordner oder die Nachricht, der verschoben oder kopiert werden soll?
    
- Wie viele der Eigenschaften des Ordners oder der Nachricht werden verschoben oder kopiert?
    
Mit den **IMAPIProp-Methoden** können Sie einen Ordner oder eine Nachricht kopieren oder verschieben. **IMAPIFolder::CopyMessages** funktioniert nur mit Nachrichten; **IMAPIFolder::CopyFolder** funktioniert nur mit Ordnern. 
  
Während die Verwendung der **IMAPIFolder-Methoden** keine Kenntnis der Eigenschaften erfordert, die vom Ordner oder der Nachricht unterstützt werden, die kopiert oder verschoben werden sollen, müssen Sie über Kenntnisse verfügen, um die **IMAPIProp-Methoden** verwenden zu können. Mit **IMAPIProp::CopyProps** müssen Sie explizit angeben können, welche der Ordner- oder Nachrichteneigenschaften Sie kopieren oder verschieben möchten. Mit **IMAPIProp::CopyTo** müssen Sie explizit angeben, welche Eigenschaften ausgeschlossen werden sollen, es sei denn, Sie möchten alle Eigenschaften kopieren oder verschieben. Weitere Informationen zu diesen Methoden finden Sie unter [Kopieren von MAPI-Eigenschaften.](copying-mapi-properties.md)
  
Die Anzahl der zu kopierenden oder zu verschiebenden Eigenschaften kann sich auf Ihre Entscheidung auswirken, welche Methode verwendet werden soll. Wenn Sie mehrere Nachrichten kopieren oder verschieben, rufen Sie **IMAPIFolder::CopyMessages auf.** Eine alternative Möglichkeit besteht darin, **IMAPIProp::CopyProps** aufzurufen, um nur die **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) -Eigenschaft des Ordners zu kopieren. Das folgende Verfahren zeigt, wie **CopyMessages** verwendet wird. 
  
### <a name="to-copy-or-move-one-or-more-messages"></a>So kopieren oder verschieben Sie eine oder mehrere Nachrichten
  
1. Suchen Sie gültige Eintragsbezeichner für die Quell- und Zielordner.
    
2. Öffnen Sie diese Ordner im Lese-/Schreibmodus, indem Sie [ENTWEDER IMAPISession::OpenEntry](imapisession-openentry.md) oder [IMsgStore::OpenEntry](imsgstore-openentry.md) aufrufen und das flag MAPI_MODIFY festlegen. 
    
3. Überprüfen Sie, ob der von **OpenEntry** zurückgegebene Schnittstellenzeiger ein **IMAPIFolder-Schnittstellenzeiger** ist. Wenn nicht, wandeln Sie ihn in den LPMAPIFOLDER-Typ um. 
    
4. Erstellen Sie ein Array von Eintragsbezeichnern, die eine oder mehrere Nachrichten darstellen, die kopiert oder verschoben werden sollen. 
    
5. Rufen Sie **IMAPIFolder::CopyMessages** auf, wobei die folgenden Flags festgelegt sind: 
    
   - MESSAGE_MOVE, wenn Sie einen Verschiebungsvorgang ausführen möchten. 
    
   - MESSAGE_DIALOG und übergeben Sie ein Fensterhandle im  _ulUIParam-Parameter,_ wenn der Ordner eine Statusanzeige anzeigen soll. 
    
6. Geben Sie die **IMAPIFolder-Zeiger** für die Quell- und Zielordner frei. 
    
Wenn Sie den vollständigen Inhalt eines Ordners in einen anderen Ordner kopieren möchten, rufen Sie die **IMAPIFolder::CopyFolder-** oder **IMAPIProp::CopyTo-Methode** des Quellordners auf. 
  
Rufen Sie zum Kopieren einiger Eigenschaften eines Ordners die **IMAPIProp::CopyProps-Methode** auf. Um die meisten Eigenschaften eines Ordners zu kopieren, rufen Sie **IMAPIProp::CopyTo** auf. 
  
Wenn Sie beispielsweise die Eigenschaften **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) und **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) eines Ordners kopieren möchten, haben Sie die folgenden Optionen:
  
- Rufen Sie **IMAPIFolder::CopyFolder** auf, um alle Ordnereigenschaften zu kopieren und dann die unerwünschten Eigenschaften aus dem neuen Ordner zu löschen. 
    
- Rufen **Sie CopyTo auf,** und schließen Sie alle Eigenschaften des Ordners mit Ausnahme von **PR_DISPLAY_NAME** und **PR_COMMENT** aus. 
    
- Rufen **Sie CopyProps auf,** und übergeben **Sie PR_DISPLAY_NAME** und **PR_COMMENT** im Include-Array. 
    
In diesem Fall ist **CopyProps** die beste Wahl, da es zum Kopieren eines kleinen Satzes von Eigenschaften verwendet werden soll und der einfachste Aufruf für die Implementierung ist. 
  
Um nur Ordnereigenschaften zu kopieren oder zu verschieben, ohne Nachrichten einzuschließen, rufen Sie die **IMAPIProp::CopyTo-Methode** des Ordners auf, und schließen Sie die folgenden Eigenschaften aus: 
  
- **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))
    
- **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))
    
Die Kopiermethoden können S_OK zurückgeben, was den Gesamterfolg, MAPI_W_PARTIAL_COMPLETION, einen teilweisen Erfolg oder einen Fehler angibt. Wenn MAPI_W_PARTIAL_COMPLETION zurückgegeben wird, verwenden Sie das **Makro HR_FAILED,** um auf einen spezifischeren Fehler zuzugreifen. Weitere Informationen finden Sie unter [Verwenden von Makros für die Fehlerbehandlung.](using-macros-for-error-handling.md)
  
Wenn Sie Nachrichten aus einem Nachrichtenspeicher in einen anderen kopieren und Unicode von beiden nicht unterstützt wird, beachten Sie, dass Informationen aufgrund der Codeseitenkonvertierung verloren gehen können. In der Regel können Sie nicht wissen, ob die Nachrichtenspeicher ein oder beide Formate unterstützen, sodass nicht ermittelt werden kann, ob Texteigenschaften als ASCII-Zeichenfolgen oder als Unicode-Zeichenfolgen kopiert werden sollen. Wenn Sie Unicode unterstützen, versuchen Sie, eine Unicode-Kopie auszuführen. wenn der Fehler mit dem Fehlerwert MAPI_E_BAD_CHARWIDTH fehlschlägt, greifen Sie auf ASCII zurück.
  

