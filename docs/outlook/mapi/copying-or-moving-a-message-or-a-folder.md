---
title: Kopieren oder Verschieben einer Nachricht oder eines Ordners
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 72290fd3-00d7-4055-bbfa-0c47b6e0f62d
description: 'Zuletzt geändert: 08 November 2011'
ms.openlocfilehash: 26fe135da93e0f5f94d9f7d264453b74f97a518b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791479"
---
# <a name="copying-or-moving-a-message-or-a-folder"></a>Kopieren oder Verschieben einer Nachricht oder eines Ordners
  
**Betrifft**: Outlook 
  
Ein Client können eine der vier Methoden zum Kopieren oder verschieben Sie eine Nachricht oder einen Ordner:
  
- [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md)
    
- [IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
    
- [IMAPIProp::CopyTo](imapiprop-copyto.md)
    
- [IMAPIProp::CopyProps](imapiprop-copyprops.md)
    
Durch Festlegen der entsprechenden Flags und Parameter, können **CopyTo** und **CopyProps** vorgenommen werden, genau wie **CopyFolder** oder **CopyMessages**arbeiten. Berücksichtigen Sie die folgenden Aspekte bei der Entscheidung, welche Methode aufgerufen:
  
- Sie kopieren oder Verschieben eines Ordners oder einer Nachricht?
    
- Wie viel wissen Sie zu dem Ordner oder eine Nachricht verschoben oder kopiert werden?
    
- Wie viele des Ordners oder des Nachrichteneigenschaften verschoben oder kopiert werden?
    
Die **IMAPIProp** Methoden können Sie kopieren oder Verschieben eines Ordners oder einer Nachricht. **IMAPIFolder::CopyMessages** ist für Nachrichten nur vorgesehen. **IMAPIFolder::CopyFolder** arbeitet mit nur Ordner. 
  
Während die Verwendung der Methoden **IMAPIFolder** nicht erforderlich sind keine Kenntnisse über die Eigenschaften, die durch den Ordner oder die Nachricht kopiert oder verschoben werden unterstützt, benötigen Sie Kenntnisse die **IMAPIProp** Methoden verwendet werden. Mit **IMAPIProp::CopyProps**müssen Sie möglicherweise explizit welche Ordner oder eine Nachricht-Eigenschaften angeben, die Sie kopieren oder verschieben möchten. Mit **IMAPIProp::CopyTo**es sei denn, Sie verwenden möchten, kopieren oder verschieben Sie alle Eigenschaften, müssen Sie explizit angeben, welche ausgeschlossen werden soll. Weitere Informationen zu diesen Methoden finden Sie unter [Kopieren von MAPI-Eigenschaften](copying-mapi-properties.md).
  
Die Anzahl der Eigenschaften kopiert oder verschoben werden, kann Ihre Entscheidung über die zu verwendende Methode auswirken. Wenn Sie kopieren oder verschieben mehrere Nachrichten, rufen Sie **IMAPIFolder::CopyMessages**. Es wird eine andere Auswahl **IMAPIProp::CopyProps** zum Kopieren von nur den Ordner **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))-Eigenschaft aufzurufen. Das folgende Verfahren zeigt, wie **CopyMessages**verwenden. 
  
### <a name="to-copy-or-move-one-or-more-messages"></a>Kopieren oder Verschieben einer oder mehrerer Nachrichten
  
1. Suchen Sie gültige-Eintragsbezeichner für die Quell- und Ziel-Ordner.
    
2. Öffnen Sie diese Ordner im Lese-/Schreibmodus durch Aufrufen von [IMAPISession::OpenEntry](imapisession-openentry.md) oder [IMsgStore::OpenEntry](imsgstore-openentry.md) und das MAPI_MODIFY-Flag festlegen. 
    
3. Überprüfen Sie, ob der von **OpenEntry** zurückgegebene Schnittstellenzeiger einen **IMAPIFolder** -Schnittstelle auf. Wenn dies nicht der Fall ist, wird es in den LPMAPIFOLDER-Typ umgewandelt. 
    
4. Erstellen Sie ein Array von Eintragsbezeichner, die eine oder mehrere Nachrichten kopiert oder verschoben werden darstellt. 
    
5. Rufen Sie mit dem folgenden Flags **IMAPIFolder::CopyMessages** : 
    
   - MESSAGE_MOVE, wenn einen Verschiebevorgang ausgeführt werden soll. 
    
   - MESSAGE_DIALOG und übergeben Sie ein Fenster behandeln im _UlUIParam_ -Parameter, wenn Sie den Ordner eine Statusanzeige anzeigen möchten. 
    
6. Freigeben Sie die **IMAPIFolder** Zeiger für die Quell- und Ziel-Ordner. 
    
Wenn Sie den vollständigen Inhalt eines Ordners in einen anderen Ordner kopieren möchten, rufen Sie **IMAPIFolder::CopyFolder** oder **IMAPIProp::CopyTo** -Methode des Quellordners. 
  
Um einige der Eigenschaften für einen Ordner zu kopieren, rufen Sie die **IMAPIProp::CopyProps** -Methode. Um die meisten Eigenschaften des Ordners zu kopieren, rufen Sie **IMAPIProp::CopyTo**. 
  
Wenn Sie eines Ordners **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) und **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) Eigenschaften kopieren möchten, müssen Sie die folgenden Optionen:
  
- Rufen Sie **IMAPIFolder::CopyFolder** zum Kopieren aller Ordnereigenschaften, und klicken Sie dann die unerwünschte Elemente aus den neuen Ordner löschen. 
    
- Rufen Sie **CopyTo** , und schließen Sie alle Eigenschaften des Ordners mit Ausnahme **PR_DISPLAY_NAME** und **PR_COMMENT aus**. 
    
- Rufen Sie **CopyProps**, übergeben Sie **PR_DISPLAY_NAME** und **PR_COMMENT** im Array einschließen. 
    
In diesem Fall **CopyProps** ist die beste Wahl, da es zum Kopieren Sie einer kleinen Gruppe von Eigenschaften verwendet werden soll und die einfachste Anruf implementieren. 
  
Zum Kopieren oder Verschieben nur die Ordnereigenschaften, ohne Nachrichten, rufen Sie den Ordner **IMAPIProp::CopyTo** -Methode und ausgeschlossen werden Sie die folgenden Eigenschaften: 
  
- **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))
    
- **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))
    
Die Copy-Methoden können S_OK, insgesamt Erfolgsmeldung MAPI_W_PARTIAL_COMPLETION, zurück, der partiellen Erfolg oder Fehler zurück. Wenn MAPI_W_PARTIAL_COMPLETION zurückgegeben wird, verwenden Sie das Makro **HR_FAILED** , um eine genauere Fehler zuzugreifen. Weitere Informationen finden Sie unter [Verwendung von Makros Fehlerbehandlung](using-macros-for-error-handling.md).
  
Wenn Sie Nachrichten von einem Informationsspeicher zu einer anderen kopieren und Unicode nicht, durch die beiden unterstützt wird, beachten Sie, dass Informationen verloren aufgrund der Konvertierung von Seiten werden kann. In der Regel können Sie nicht wissen, wenn die Nachrichtenspeicher für eine oder beide Formate unterstützen leicht zu bestimmen, ob Eigenschaften als ASCII-Zeichenfolgen oder als Unicode-Zeichenfolgen mit Text kopieren nicht möglich. Wenn Unicode unterstützt werden, versuchen Sie, eine Kopie des Unicode-ausführen. Wenn sie mit den Fehlerwert MAPI_E_BAD_CHARWIDTH fehlschlägt, greifen Sie auf ASCII.
  

