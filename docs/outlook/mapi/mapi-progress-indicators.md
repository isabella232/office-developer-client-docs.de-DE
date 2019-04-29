---
title: MAPI-fortSchrittsIndikatoren
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
# <a name="mapi-progress-indicators"></a>MAPI-fortSchrittsIndikatoren

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Viele der Vorgänge, die Sie für Clients ausführen, können sehr viel Zeit in Anspruch nehmen. Wenn Sie Clients über den Fortschritt eines längeren Vorgangs informieren möchten, können Sie einen Indikator anzeigen, der den abgeschlossenen Teil eines Vorgangs zu einem beliebigen Zeitpunkt vom Beginn des Vorgangs bis zum Abschluss grafisch anzeigt. Die Fortschrittsanzeige zeigt einen Prozentsatz der gesamten auszufüllenden Operation an.
  
Die folgenden Methoden unterstützen langwierige Vorgänge und die Anzeige einer Statusanzeige:
  
- [IMAPIFolder:: CopyMessages](imapifolder-copymessages.md), [IMAPIFolder:: CopyFolder](imapifolder-copyfolder.md), [IMAPIFolder::D Eletemessages](imapifolder-deletemessages.md), [IMAPIFolder::D Eletefolder](imapifolder-deletefolder.md), [IMAPIFolder:: EmptyFolder](imapifolder-emptyfolder.md)und [IMAPIFolder:: SetReadFlags](imapifolder-setreadflags.md).
    
- [IMAPIProp:: CopyProps](imapiprop-copyprops.md) und [IMAPIProp:: CopyTo](imapiprop-copyto.md).
    
- [IMAPISupport::D ocopyprops](imapisupport-docopyprops.md), [IMAPISupport::D ocopyto](imapisupport-docopyto.md), [IMAPISupport:: CopyFolder](imapisupport-copyfolder.md)und [IMAPISupport:: CopyMessages](imapisupport-copymessages.md).
    
- [IMessage::D eleteattach](imessage-deleteattach.md).
    
- [IABContainer:: CopyEntries](iabcontainer-copyentries.md).
    
Um eine Statusanzeige anzuzeigen, definiert MAPI ein Progress-Objekt. Progress-Objekte implementieren die [IMAPIProgress: IUnknown](imapiprogressiunknown.md) -Schnittstelle, eine Schnittstelle, die Methoden zum Festlegen des Indikators und zum Erstellen der Anzeige enthält. MAPI bietet eine Progress-Objekt Implementierung wie einige Clients. Sie sollten die Implementierung eines Clients, sofern vorhanden, als Eingabeparameter für die Methode verwenden, die den Vorgang ausführt. Wenn der Client NULL anstelle eines Zeigers an ein Progress-Objekt übergibt, verwenden Sie die MAPI-Implementierung, indem Sie die [IMAPISupport::D oprogressdialog](imapisupport-doprogressdialog.md) -Methode aufrufen. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Dienstanbieter](mapi-service-providers.md)

