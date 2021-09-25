---
title: MAPI-Fortschrittsindikatoren
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 73a99e52-97fe-40f5-af90-52cfd858ab22
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d1317290b99fe3e10dec539e0a349382cc880188
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575645"
---
# <a name="mapi-progress-indicators"></a>MAPI-Fortschrittsindikatoren

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Viele der Vorgänge, die Sie für Clients ausführen, können sehr viel Zeit in Anspruch nehmen. Um Clients über den Fortschritt eines langen Vorgangs zu informieren, können Sie einen Indikator anzeigen, der den abgeschlossenen Teil eines Vorgangs zu einem beliebigen Zeitpunkt vom Beginn des Vorgangs bis zum Abschluss grafisch anzeigt. Die Statusanzeige zeigt einen Prozentsatz des gesamten Vorgangs an, der abgeschlossen werden soll.
  
Die folgenden Methoden unterstützen lange Vorgänge und die Anzeige einer Statusanzeige:
  
- [IMAPIFolder::CopyMessages](imapifolder-copymessages.md), [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md), [IMAPIFolder::D eleteMessages](imapifolder-deletemessages.md), [IMAPIFolder::D eleteFolder](imapifolder-deletefolder.md), [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md)und [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md).
    
- [IMAPIProp::CopyProps](imapiprop-copyprops.md) und [IMAPIProp::CopyTo](imapiprop-copyto.md).
    
- [IMAPISupport::D oCopyProps](imapisupport-docopyprops.md), [IMAPISupport::D oCopyTo](imapisupport-docopyto.md), [IMAPISupport::CopyFolder](imapisupport-copyfolder.md)und [IMAPISupport::CopyMessages](imapisupport-copymessages.md).
    
- [IMessage::D eleteAttach](imessage-deleteattach.md).
    
- [IABContainer::CopyEntries](iabcontainer-copyentries.md).
    
Um eine Statusanzeige anzuzeigen, definiert MAPI ein Statusobjekt. Progress-Objekte implementieren die [IMAPIProgress : IUnknown-Schnittstelle,](imapiprogressiunknown.md) eine Schnittstelle, die Methoden zum Einrichten des Bereichs des Indikators und zum Erstellen der Anzeige enthält. MAPI bietet eine Fortschrittsobjektimplementierungen wie einige Clients. Sie sollten die Implementierung eines Clients, falls vorhanden, als Eingabeparameter für die Methode verwenden, die den Vorgang ausführt. Wenn der Client NULL anstelle eines Zeigers an ein Statusobjekt übergibt, verwenden Sie die MAPI-Implementierung, indem Sie die [IMAPISupport::D oProgressDialog-Methode](imapisupport-doprogressdialog.md) aufrufen. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Dienstanbieter](mapi-service-providers.md)

