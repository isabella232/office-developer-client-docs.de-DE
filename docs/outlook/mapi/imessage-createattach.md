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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417671"
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
  
> [in] Zeiger auf die Schnittstellen-ID (Interface Identifier, IID), die die Schnittstelle darstellt, die für den Zugriff auf die Nachricht verwendet werden soll. Das Übergeben von NULL führt dazu, dass die Standardschnittstelle der Nachricht oder **IMessage** zurückgegeben wird. 
    
 _ulFlags_
  
> [in] Bitmaske von Flags, die steuert, wie die Anlage erstellt wird. Das folgende Flag kann festgelegt werden:
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht **createAttach,** erfolgreich zurückzukehren, möglicherweise bevor der Zugriff auf die Anlage für den aufrufenden Client vollständig möglich ist. Wenn auf die Anlage nicht zugegriffen werden kann, kann ein nachfolgender Aufruf zu einem Fehler führen. 
    
 _lpulAttachmentNum_
  
> [out] Zeiger auf eine Indexnummer, die die neu erstellte Anlage identifiziert. Diese Zahl ist nur gültig, wenn die Nachricht geöffnet ist und die Basis für die **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) -Eigenschaft der Anlage ist.
    
 _lppAttach_
  
> [out] Zeiger auf einen Zeiger auf das geöffnete Anlagenobjekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Anlage wurde erfolgreich erstellt.
    
## <a name="remarks"></a>Hinweise

Die **IMessage::CreateAttach-Methode** erstellt eine neue Anlage für eine Nachricht. Die neue Anlage und alle dafür festgelegten Eigenschaften sind erst verfügbar, wenn ein Client sowohl die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) der Anlage als auch die **IMAPIProp::SaveChanges-Methode der** Nachricht aufgerufen hat. 
  
Die anlagenummer, auf die  _von lpulAttachmentNum_ verwiesen wird, ist eindeutig und nur im Kontext der Nachricht gültig. Das heißt, zwei Anlagen in zwei verschiedenen Nachrichten können dieselbe Nummer haben, während zwei Anlagen in derselben Nachricht nicht möglich sind. 
  
## <a name="see-also"></a>Siehe auch



[IMessage: IMAPIProp](imessageimapiprop.md)

