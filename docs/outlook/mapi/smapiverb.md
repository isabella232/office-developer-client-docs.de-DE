---
title: SMAPIVerb
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SMAPIVerb
api_type:
- COM
ms.assetid: 45066528-2447-4178-aaa3-7513ed0b3ba4
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 68c77f60abdb00a9df4aed4afd60401bad239756
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629564"
---
# <a name="smapiverb"></a>SMAPIVerb

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt ein MAPI-Verb.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiform.h  <br/> |
   
```cpp
typedef struct
{
  ULONG lVerb;
  LPSTR szVerbname;
  DWORD fuFlags;
  DWORD grfAttribs;
  ULONG ulFlags; /* Either 0 or MAPI_UNICODE */
} SMAPIVerb, FAR * LPMAPIVERB;

```

## <a name="members"></a>Members

 **lVerb**
  
> Code, der das Verb darstellt, das an [IMAPIForm::D oVerb](imapiform-doverb.md)übergeben wird. Standardverben werden in der Headerdatei Exchform.h definiert.
    
 **szVerbname**
  
> Anzeigename des Verbs, wie er im Formularmenü angezeigt wird.
    
 **fuFlags**
  
> Flags für das Verb.
    
 **grfAttribs**
  
> Attribute des Verbs. 
    
 **ulFlags**
  
> Flag, das das Format des Anzeigenamens des Verbs angibt. Das folgende Kennzeichen kann festgelegt werden:
    
MAPI_UNICODE 
  
> Der Anzeigename hat das Unicode-Format. Wenn das MAPI_UNICODE-Kennzeichen nicht festgelegt ist, hat der Anzeigename das ANSI-Format.
    
## <a name="remarks"></a>Bemerkungen

Die **SMAPIVerb-Struktur** wird in den folgenden Methoden als Parameter übergeben: 
  
- [IMAPIFormContainer::ResolveMultipleMessageClasses](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [IMAPIFormMgr::ResolveMultipleMessageClasses](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a>Siehe auch



[CbMessageClassArray](cbmessageclassarray.md)


[MAPI-Strukturen](mapi-structures.md)

