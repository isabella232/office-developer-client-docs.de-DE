---
title: IMessageCreateAttach
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.IMessage::CreateAttach
api_type:
- COM
ms.assetid: 01711aca-c598-438c-88d7-0719b6691e34
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 22735e5d165fb61043bb6433ba84567bf1b3f957
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567361"
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
  
> [in] Zeiger auf den Schnittstellenbezeichner (IID), der die Schnittstelle darstellt, die für den Zugriff auf die Nachricht verwendet werden soll. Das Übergeben von NULL führt dazu, dass die Standardschnittstelle der Nachricht oder **IMessage** zurückgegeben wird. 
    
 _ulFlags_
  
> [in] Bitmaske von Flags, die steuert, wie die Anlage erstellt wird. Das folgende Kennzeichen kann festgelegt werden:
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht **CreateAttach** die erfolgreiche Rückgabe, möglicherweise bevor der aufrufende Client vollständig auf die Anlage zugegriffen werden kann. Wenn auf die Anlage nicht zugegriffen werden kann, kann ein nachfolgender Aufruf zu einem Fehler führen. 
    
 _lpulAttachmentNum_
  
> [out] Zeiger auf eine Indexnummer, die die neu erstellte Anlage identifiziert. Diese Zahl ist nur gültig, wenn die Nachricht geöffnet ist und die Basis für die **eigenschaft PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) der Anlage ist.
    
 _lppAttach_
  
> [out] Zeiger auf einen Zeiger auf das geöffnete Anlagenobjekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Anlage wurde erfolgreich erstellt.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMessage::CreateAttach-Methode** erstellt eine neue Anlage für eine Nachricht. Die neue Anlage und alle dafür festgelegten Eigenschaften sind erst verfügbar, wenn ein Client die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) der Anlage und die **IMAPIProp::SaveChanges-Methode** der Nachricht aufgerufen hat. 
  
Die Anlagennummer, auf die von  _lpulAttachmentNum_ verwiesen wird, ist eindeutig und nur im Kontext der Nachricht gültig. Das heißt, zwei Anlagen in zwei verschiedenen Nachrichten können dieselbe Nummer haben, während zwei Anlagen in derselben Nachricht dies nicht können. 
  
## <a name="see-also"></a>Siehe auch



[IMessage: IMAPIProp](imessageimapiprop.md)

