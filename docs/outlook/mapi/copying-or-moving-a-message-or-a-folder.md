---
title: Kopieren oder Verschieben einer Nachricht oder eines Ordners
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 72290fd3-00d7-4055-bbfa-0c47b6e0f62d
description: 'Letzte Änderung: 08. November 2011'
ms.openlocfilehash: c5e92c44d7078560ed84d72b3477d5cf2e809353
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413500"
---
# <a name="copying-or-moving-a-message-or-a-folder"></a>Kopieren oder Verschieben einer Nachricht oder eines Ordners
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Client kann eine von vier Methoden verwenden, um eine Nachricht oder einen Ordner zu kopieren oder zu verschieben:
  
- [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md)
    
- [IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
    
- [IMAPIProp::CopyTo](imapiprop-copyto.md)
    
- [IMAPIProp::CopyProps](imapiprop-copyprops.md)
    
Durch Festlegen der entsprechenden Flags und Parameter können **CopyTo** und **CopyProps** wie **CopyFolder** oder **CopyMessages funktionieren.** Berücksichtigen Sie die folgenden Probleme bei der Entscheidung, welche Methode sie aufrufen soll:
  
- Kopieren oder verschieben Sie einen Ordner oder eine Nachricht?
    
- Wie viel wissen Sie über den Ordner oder die Nachricht, der verschoben oder kopiert werden soll?
    
- Wie viele Eigenschaften des Ordners oder der Nachricht werden verschoben oder kopiert?
    
Sie können die **IMAPIProp-Methoden** verwenden, um einen Ordner oder eine Nachricht zu kopieren oder zu verschieben. **IMAPIFolder::CopyMessages** kann nur mit Nachrichten verwendet werden. **IMAPIFolder::CopyFolder funktioniert** nur mit Ordnern. 
  
Während die Verwendung der **IMAPIFolder-Methoden** keine Kenntnisse der eigenschaften erfordert, die vom Ordner oder der Nachricht unterstützt werden, um kopiert oder verschoben zu werden, müssen Sie über einige Kenntnisse verfügen, um die **IMAPIProp-Methoden verwenden zu** können. Mit **IMAPIProp::CopyProps** müssen Sie explizit angeben können, welche der Ordner- oder Nachrichteneigenschaften Sie kopieren oder verschieben möchten. Mit **IMAPIProp::CopyTo** müssen Sie explizit angeben, welche Eigenschaften ausgeschlossen werden sollen, es sei denn, Sie möchten alle Eigenschaften kopieren oder verschieben. Weitere Informationen zu diesen Methoden finden Sie unter [Kopieren von MAPI-Eigenschaften](copying-mapi-properties.md).
  
Die Anzahl der zu kopierenden oder zu verschobenen Eigenschaften kann sich auf Ihre Entscheidung über die zu verwendende Methode auswirken. Wenn Sie mehrere Nachrichten kopieren oder verschieben, rufen Sie **IMAPIFolder::CopyMessages auf.** Alternativ können Sie **IMAPIProp::CopyProps** aufrufen, um nur die **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) des Ordners zu kopieren. Im folgenden Verfahren wird die Verwendung von **CopyMessages veranschaulicht.** 
  
### <a name="to-copy-or-move-one-or-more-messages"></a>So kopieren oder verschieben Sie eine oder mehrere Nachrichten
  
1. Suchen Sie nach gültigen Eintragsbezeichnern für die Quell- und Zielordner.
    
2. Öffnen Sie diese Ordner im Lese-/Schreibmodus, indem Sie [entweder IMAPISession::OpenEntry](imapisession-openentry.md) oder [IMsgStore::OpenEntry](imsgstore-openentry.md) aufrufen und das MAPI_MODIFY festlegen. 
    
3. Überprüfen Sie, ob der von **OpenEntry zurückgegebene Schnittstellenzeiger** ein **IMAPIFolder-Schnittstellenzeiger** ist. Andern falls nicht, wird es in den LPMAPIFOLDER-Typ umgeknapst. 
    
4. Erstellen Sie ein Array von Eintragsbezeichnern, die eine oder mehrere Nachrichten darstellen, die kopiert oder verschoben werden sollen. 
    
5. Rufen **Sie IMAPIFolder::CopyMessages mit** den folgenden Flags auf: 
    
   - MESSAGE_MOVE, wenn Sie einen Verschiebevorgang ausführen möchten. 
    
   - MESSAGE_DIALOG und übergeben Sie ein Fensterhandle im  _ulUIParam-Parameter,_ wenn der Ordner eine Statusanzeige anzeigen soll. 
    
6. Geben Sie **die IMAPIFolder-Zeiger** für die Quell- und Zielordner frei. 
    
Wenn Sie den vollständigen Inhalt eines Ordners in einen anderen Ordner kopieren möchten, rufen Sie die **IMAPIFolder::CopyFolder-** oder **IMAPIProp::CopyTo-Methode** des Quellordners auf. 
  
Rufen Sie die **IMAPIProp::CopyProps-Methode** auf, um einige Eigenschaften eines Ordners zu kopieren. Um die meisten Eigenschaften eines Ordners zu kopieren, rufen Sie **IMAPIProp::CopyTo auf.** 
  
Wenn Sie beispielsweise die Eigenschaften **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) und **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) eines Ordners kopieren möchten, haben Sie die folgenden Optionen:
  
- Rufen **Sie IMAPIFolder::CopyFolder auf,** um alle Ordnereigenschaften zu kopieren und die unerwünschten Eigenschaften dann aus dem neuen Ordner zu löschen. 
    
- Rufen **Sie CopyTo** auf, und schließen Sie alle Eigenschaften des Ordners aus, mit Ausnahme von **PR_DISPLAY_NAME** und **PR_COMMENT**. 
    
- Rufen **Sie CopyProps** auf, **PR_DISPLAY_NAME** und **PR_COMMENT** im include-Array übergeben. 
    
In diesem Fall ist **CopyProps** die beste Wahl, da es zum Kopieren einer kleinen Gruppe von Eigenschaften verwendet werden soll und der einfachste Aufruf zur Implementierung ist. 
  
Um nur Ordnereigenschaften zu kopieren oder zu verschieben, ohne Nachrichten zu enthalten, rufen Sie die **IMAPIProp::CopyTo-Methode** des Ordners auf, und schließen Sie die folgenden Eigenschaften aus: 
  
- **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))
    
- **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))
    
Die Kopiermethoden können S_OK zurückgeben, was den Gesamterfolg angibt, MAPI_W_PARTIAL_COMPLETION, einen Teilerfolg oder einen Fehler angibt. Wenn MAPI_W_PARTIAL_COMPLETION zurückgegeben wird, verwenden Sie **HR_FAILED** Makro, um auf einen spezifischeren Fehler zu zugreifen. Weitere Informationen finden Sie unter [Using Macros for Error Handling](using-macros-for-error-handling.md).
  
Wenn Sie Nachrichten aus einem Nachrichtenspeicher in einen anderen kopieren und Unicode von beiden nicht unterstützt wird, beachten Sie, dass Informationen aufgrund der Codeseitenkonvertierung verloren gehen können. In der Regel können Sie nicht wissen, ob die Nachrichtenspeicher ein oder beide Formate unterstützen, was es unmöglich macht, zu bestimmen, ob Texteigenschaften als ASCII-Zeichenfolgen oder als Unicode-Zeichenfolgen kopiert werden. Wenn Sie Unicode unterstützen, versuchen Sie, eine #A0 durchzuführen. Wenn ein Fehler mit dem Fehlerwert MAPI_E_BAD_CHARWIDTH, greifen Sie auf ASCII zurück.
  

