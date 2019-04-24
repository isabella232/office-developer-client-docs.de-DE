---
title: IMessageCreateAttach
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.IMessage::CreateAttach
api_type:
- COM
ms.assetid: 01711aca-c598-438c-88d7-0719b6691e34
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f534912377aadb3c342030fc02fce26693857476
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351114"
---
# <a name="imessagecreateattach"></a>IMessage::CreateAttach

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt eine neue Anlage.
  
```cpp
HRESULT CreateAttach(
LPCIID lpInterface,
ULONG ulFlags,
ULONG FAR * lpulAttachmentNum,
LPATTACH FAR * lppAttach
);
```

## <a name="parameters"></a>Parameter

 _lpInterface_
  
> in Zeiger auf die Schnittstellen-ID (IID), die die Schnittstelle darstellt, die für den Zugriff auf die Nachricht verwendet werden soll. Übergeben von NULL-Ergebnissen in der Standardschnittstelle der Nachricht oder **IMessage**, wird zurückgegeben. 
    
 _ulFlags_
  
> in Bitmaske von Flags, die die Erstellung der Anlage steuert. Das folgende Flag kann festgelegt werden:
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht **** , dass createattach erfolgreich zurückgegeben wird, möglicherweise, bevor der aufrufende Client vollständig auf die Anlage zugreifen kann. Wenn auf die Anlage nicht zugegriffen werden kann, führt der nachfolgende Aufruf zu einem Fehler. 
    
 _lpulAttachmentNum_
  
> Out Zeiger auf eine Indexnummer, die die neu erstellte Anlage identifiziert. Diese Nummer ist nur gültig, wenn die Nachricht geöffnet ist und die Grundlage für die **PR_ATTACH_NUM** ([pidtagattachnumber (](pidtagattachnumber-canonical-property.md))-Eigenschaft der Anlage ist.
    
 _lppAttach_
  
> Out Zeiger auf einen Zeiger auf das offene Attachment-Objekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Anlage wurde erfolgreich erstellt.
    
## <a name="remarks"></a>Bemerkungen

Die **IMessage:: createattach** -Methode erstellt eine neue Anlage für eine Nachricht. Die neue Anlage und alle für Sie festgelegten Eigenschaften sind erst verfügbar, wenn ein Client sowohl die [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode als auch die **IMAPIProp:: SaveChanges** -Methode der Nachricht aufgerufen hat. 
  
Die Anlagennummer, auf die durch _lpulAttachmentNum_ verwiesen wird, ist eindeutig und gilt nur innerhalb des Kontexts der Nachricht. Das heißt, zwei Anlagen in zwei verschiedenen Nachrichten können dieselbe Anzahl haben, während zwei Anlagen in der gleichen Nachricht nicht. 
  
## <a name="see-also"></a>Siehe auch



[IMessage: IMAPIProp](imessageimapiprop.md)

