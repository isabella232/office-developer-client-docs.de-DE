---
title: SMAPIVerb
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIVerb
api_type:
- COM
ms.assetid: 45066528-2447-4178-aaa3-7513ed0b3ba4
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 4d060d62deb685b4691846c2b8e48a82ae3195ea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795599"
---
# <a name="smapiverb"></a>SMAPIVerb

  
  
**Betrifft**: Outlook 
  
Beschreibt ein MAPI-Verb an.
  
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

## <a name="members"></a>Elemente

 **lVerb**
  
> Code, der das Verb an, das an [IMAPIForm::DoVerb](imapiform-doverb.md)übergeben wird, darstellt. Standard-Verben sind in der Headerdatei Exchform.h definiert.
    
 **szVerbname**
  
> Anzeigename des Verbs, die im Formular angezeigt wird.
    
 **fuFlags**
  
> Flags für das Verb.
    
 **grfAttribs**
  
> Attribute des Verbs. 
    
 **ulFlags**
  
> Kennzeichen Sie, die das Format des Anzeigenamens des Verbs. Das folgende Flag kann festgelegt werden:
    
PARAMETER MAPI_UNICODE 
  
> Der Anzeigename ist im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, ist der Anzeigename im ANSI-Format.
    
## <a name="remarks"></a>Bemerkungen

Die Struktur **SMAPIVerb** wird als Parameter in der folgenden Methoden übergeben: 
  
- [IMAPIFormContainer::ResolveMultipleMessageClasses](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [IMAPIFormMgr::ResolveMultipleMessageClasses](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a>Siehe auch



[CbMessageClassArray](cbmessageclassarray.md)


[MAPI-Strukturen](mapi-structures.md)

