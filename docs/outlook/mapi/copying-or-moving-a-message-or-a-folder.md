---
title: Kopieren oder Verschieben einer Nachricht oder eines Ordners
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 72290fd3-00d7-4055-bbfa-0c47b6e0f62d
description: 'Zuletzt geändert: 20 November, 2011'
ms.openlocfilehash: c5e92c44d7078560ed84d72b3477d5cf2e809353
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413500"
---
# <a name="copying-or-moving-a-message-or-a-folder"></a>Kopieren oder Verschieben einer Nachricht oder eines Ordners
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Client kann eine der vier Methoden zum Kopieren oder Verschieben einer Nachricht oder eines Ordners verwenden:
  
- [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md)
    
- [IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
    
- [IMAPIProp::CopyTo](imapiprop-copyto.md)
    
- [IMAPIProp::CopyProps](imapiprop-copyprops.md)
    
Durch Festlegen der entsprechenden Flags und Parameter können **CopyTo** und **CopyProps** wie **CopyFolder** oder **CopyMessages**ausgeführt werden. Berücksichtigen Sie bei der Entscheidung, welche Methode aufgerufen werden soll, die folgenden Probleme:
  
- Kopieren oder bewegen Sie einen Ordner oder eine Nachricht?
    
- Wie viel wissen Sie über den Ordner oder die Nachricht, der verschoben oder kopiert werden soll?
    
- Wie viele der Eigenschaften des Ordners oder der Nachricht werden verschoben oder kopiert?
    
Sie können die **IMAPIProp** -Methoden verwenden, um einen Ordner oder eine Nachricht zu kopieren oder zu verschieben. **IMAPIFolder:: CopyMessages** funktioniert nur mit Nachrichten; **IMAPIFolder:: CopyFolder** funktioniert nur mit Ordnern. 
  
Während die Verwendung der **IMAPIFolder** -Methoden keine Kenntnis der vom Ordner oder der zu verschiebenden Nachricht unterstützten Eigenschaften erfordert, müssen Sie über Kenntnisse verfügen, um die **IMAPIProp** -Methoden verwenden zu können. Mit **IMAPIProp:: CopyProps**müssen Sie in der Lage sein, explizit anzugeben, welche der Ordner-oder Nachrichteneigenschaften Sie kopieren oder verschieben möchten. Wenn Sie alle Eigenschaften mit **IMAPIProp:: CopyTo**kopieren oder verschieben möchten, müssen Sie explizit angeben, welche davon ausgeschlossen werden sollen. Weitere Informationen zu diesen Methoden finden Sie unter [Kopieren von MAPI-Eigenschaften](copying-mapi-properties.md).
  
Die Anzahl der Eigenschaften, die kopiert oder verschoben werden können, kann sich auf die Entscheidung für die zu verwendende Methode auswirken. Wenn Sie mehrere Nachrichten kopieren oder ändern, rufen Sie **IMAPIFolder:: CopyMessages**auf. Alternativ können Sie **IMAPIProp:: CopyProps** aufrufen, um nur die **PR_CONTAINER_CONTENTS** ([pidtagcontainercontents (](pidtagcontainercontents-canonical-property.md))-Eigenschaft des Ordners zu kopieren. Im folgenden Verfahren wird gezeigt, wie Sie **CopyMessages**verwenden. 
  
### <a name="to-copy-or-move-one-or-more-messages"></a>So kopieren oder verschieben Sie eine oder mehrere Nachrichten
  
1. Suchen gültiger Eintragsbezeichner für die Quell-und Zielordner.
    
2. Öffnen Sie diese Ordner im Lese-/Schreibzugriff, indem Sie entweder [IMAPISession:: OpenEntry](imapisession-openentry.md) oder [IMsgStore:: OpenEntry](imsgstore-openentry.md) aufrufen und das MAPI_MODIFY-Flag festlegen. 
    
3. Stellen Sie sicher, dass der von **OpenEntry** zurückgegebene Schnittstellenzeiger ein **IMAPIFolder** -Schnittstellenzeiger ist. Wenn dies nicht der Fall ist, wandeln Sie ihn in den LPMAPIFOLDER-Typ um. 
    
4. Erstellen Sie ein Array von Eintrags Bezeichnern, die die eine oder mehrere Nachrichten darstellen, die kopiert oder verschoben werden. 
    
5. Rufen Sie **IMAPIFolder:: CopyMessages** auf, wobei die folgenden Flags festgelegt sind: 
    
   - MESSAGE_MOVE, wenn Sie einen Verschiebungsvorgang ausführen möchten. 
    
   - MESSAGE_DIALOG, und übergeben Sie ein Fensterhandle im _ulUIParam_ -Parameter, wenn der Ordner eine Statusanzeige anzeigen soll. 
    
6. Geben Sie die **IMAPIFolder** -Zeiger für die Quell-und Zielordner frei. 
    
Wenn Sie den vollständigen Inhalt eines Ordners in einen anderen Ordner kopieren möchten, rufen Sie die **IMAPIFolder:: CopyFolder** -oder **IMAPIProp:: CopyTo** -Methode des Quellordners auf. 
  
Rufen Sie die **IMAPIProp:: CopyProps** -Methode auf, um einige der Eigenschaften eines Ordners zu kopieren. Um die meisten Eigenschaften eines Ordners zu kopieren, rufen Sie **IMAPIProp:: CopyTo**auf. 
  
Wenn Sie beispielsweise die Eigenschaften **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) und **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) eines Ordners kopieren möchten, haben Sie folgende Möglichkeiten:
  
- Rufen Sie **IMAPIFolder:: CopyFolder** auf, um alle Ordner Eigenschaften zu kopieren und die unerwünschten Dateien aus dem neuen Ordner zu löschen. 
    
- Rufen Sie **CopyTo** auf, und schließen Sie alle Eigenschaften des Ordners außer für **PR_DISPLAY_NAME** und **PR_COMMENT**aus. 
    
- Rufen Sie **CopyProps**auf, und übergeben Sie **PR_DISPLAY_NAME** und **PR_COMMENT** im Include-Array. 
    
In diesem Fall ist **CopyProps** die beste Wahl, da es verwendet werden soll, um eine kleine Gruppe von Eigenschaften zu kopieren und am einfachsten zu implementieren ist. 
  
Um nur Ordner Eigenschaften zu kopieren oder zu verschieben, ohne Nachrichten hinzufügen, rufen Sie die **IMAPIProp:: CopyTo** -Methode des Ordners auf, und schließen Sie die folgenden Eigenschaften aus: 
  
- **PR_CONTAINER_CONTENTS** ([Pidtagcontainercontents (](pidtagcontainercontents-canonical-property.md))
    
- **PR_FOLDER_ASSOCIATED_CONTENTS** ([Pidtagfolderassociatedcontents (](pidtagfolderassociatedcontents-canonical-property.md))
    
Die Copy-Methoden können S_OK zurückgeben, was bedeutet, dass der gesamte Erfolg, MAPI_W_PARTIAL_COMPLETION, der teilweiser Erfolg angibt, oder ein Fehler. Wenn MAPI_W_PARTIAL_COMPLETION zurückgegeben wird, verwenden Sie das **HR_FAILED** -Makro, um auf einen spezifischeren Fehler zuzugreifen. Weitere Informationen finden Sie unter [Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md).
  
Wenn Sie Nachrichten aus einem Nachrichtenspeicher in einen anderen kopieren und Unicode von beiden nicht unterstützt wird, beachten Sie, dass Informationen aufgrund der Konvertierung von Codeseiten verloren gehen können. In der Regel können Sie nicht wissen, ob die Nachrichtenspeicher ein oder beide Formate unterstützen, sodass es unmöglich ist, zu bestimmen, ob Texteigenschaften als ASCII-Zeichenfolgen oder als Unicode-Zeichenfolgen kopiert werden sollen. Wenn Sie Unicode unterstützen, versuchen Sie, eine Unicode-Kopie auszuführen. Wenn Sie mit dem Fehlerwert MAPI_E_BAD_CHARWIDTH fehlschlägt, greifen Sie auf ASCII zu.
  

