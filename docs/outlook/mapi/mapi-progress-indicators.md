---
title: MAPI-Fortschrittsindikatoren
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 73a99e52-97fe-40f5-af90-52cfd858ab22
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: cdfb6898146583b7da9b043eadd3acc09edbf292
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410707"
---
# <a name="mapi-progress-indicators"></a>MAPI-Fortschrittsindikatoren

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Viele der Vorgänge, die Sie für Clients ausführen, können sehr lange dauern. Um Clients über den Fortschritt eines langwierigen Vorgangs zu informieren, können Sie einen Indikator anzeigen, der den fertigen Teil eines Vorgangs an einem bestimmten Punkt vom Beginn des Vorgangs bis zum Abschluss grafisch anzeigt. Der Fortschrittsindikator zeigt einen Prozentsatz des gesamten vorgangs an, der abgeschlossen werden soll.
  
Die folgenden Methoden unterstützen langwierige Vorgänge und die Anzeige eines Statusindikators:
  
- [IMAPIFolder::CopyMessages](imapifolder-copymessages.md), [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md), [IMAPIFolder::D eleteMessages](imapifolder-deletemessages.md), [IMAPIFolder::D eleteFolder](imapifolder-deletefolder.md), [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md)und [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md).
    
- [IMAPIProp::CopyProps](imapiprop-copyprops.md) und [IMAPIProp::CopyTo](imapiprop-copyto.md).
    
- [IMAPISupport::D oCopyProps](imapisupport-docopyprops.md), [IMAPISupport::D oCopyTo](imapisupport-docopyto.md), [IMAPISupport::CopyFolder](imapisupport-copyfolder.md)und [IMAPISupport::CopyMessages](imapisupport-copymessages.md).
    
- [IMessage::D eleteAttach](imessage-deleteattach.md).
    
- [IABContainer::CopyEntries](iabcontainer-copyentries.md).
    
Zum Anzeigen eines Statusindikators definiert MAPI ein Statusobjekt. Progress-Objekte implementieren die [IMAPIProgress : IUnknown-Schnittstelle,](imapiprogressiunknown.md) eine Schnittstelle, die Methoden zum Festlegen des Indikatorbereichs und zum Erstellen der Anzeige enthält. MAPI stellt eine Progress-Objektimplementierung wie einige Clients zur Verfügung. Wenn eine Clientimplementierung angegeben wird, sollten Sie die Implementierung eines Clients als Eingabeparameter für die Methode verwenden, mit der der Vorgang ausgeführt wird. Wenn der Client NULL anstelle eines Zeigers auf ein Progress-Objekt übergibt, verwenden Sie die MAPI-Implementierung, indem Sie die [IMAPISupport::D oProgressDialog-Methode](imapisupport-doprogressdialog.md) aufrufen. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Dienstanbieter](mapi-service-providers.md)

