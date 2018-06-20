---
title: MAPI-Statusanzeigen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 73a99e52-97fe-40f5-af90-52cfd858ab22
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d8af2ba3067dabe759056313eb278b9901510980
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793043"
---
# <a name="mapi-progress-indicators"></a>MAPI-Statusanzeigen

  
  
**Betrifft**: Outlook 
  
Viele Vorgänge, die Sie für Clients ausführen dauert sehr lange Zeit in Anspruch. Um den Fortschritt eines längeren Vorgangs-Clients zu informieren, können Sie ein Symbol anzeigen, das den Teil eines Vorgangs nach Abschluss des Vorgangs zu einem bestimmten Zeitpunkt vom Anfang des Vorgangs zu ihrem Abschluss grafisch dargestellt werden. Die Statusanzeige zeigt einen prozentualen Anteil der gesamte Vorgang ausgeführt werden.
  
Die folgenden Methoden unterstützen langen Vorgänge und die Anzeige einer Statusanzeige:
  
- [IMAPIFolder::CopyMessages](imapifolder-copymessages.md), [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md), [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md), [IMAPIFolder::DeleteFolder](imapifolder-deletefolder.md), [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md)und [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md).
    
- [IMAPIProp::CopyProps](imapiprop-copyprops.md) und [IMAPIProp::CopyTo](imapiprop-copyto.md).
    
- [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md), [IMAPISupport::DoCopyTo](imapisupport-docopyto.md), [IMAPISupport::CopyFolder](imapisupport-copyfolder.md)und [IMAPISupport::CopyMessages](imapisupport-copymessages.md).
    
- [IMessage::DeleteAttach](imessage-deleteattach.md).
    
- [IABContainer::CopyEntries](iabcontainer-copyentries.md).
    
Zum Anzeigen einer Statusanzeige definiert MAPI ein Fortschritt-Objekt. Fortschritt Objekte Implementieren der [IMAPIProgress: IUnknown](imapiprogressiunknown.md) -Schnittstelle, die eine Schnittstelle, die Methoden für das Einrichten des Bereichs von den Indikator und die Anzeige erstellen enthält. MAPI bietet eine Implementierung der Fortschritt-Objekt, wie einige Clients. Sie sollten eine Client-Implementierung verwenden, wenn eine bereitgestellt wird, als Eingabeparameter der Methode Ausführen des Vorgangs. Wenn der Client NULL anstatt einen Zeiger auf ein Objekt Fortschritt übergibt, verwenden Sie des MAPI-Implementierung durch Aufrufen der [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) -Methode. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Dienstanbieter](mapi-service-providers.md)

