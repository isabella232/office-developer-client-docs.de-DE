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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3ef284a2c036abb9eac10ecf33de4adbf61f3c54
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410959"
---
# <a name="smapiverb"></a>SMAPIVerb

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt ein MAPI-Verb.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiform. h  <br/> |
   
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
  
> Code, der das Verb darstellt, das an IMAPIForm übergeben wird [::D overb](imapiform-doverb.md). Standard Verben werden in der Headerdatei Exchform. h definiert.
    
 **szVerbname**
  
> Anzeigename des Verbs, wie er im Menü Formular angezeigt wird.
    
 **fuFlags**
  
> Kennzeichen für das Verb.
    
 **grfAttribs**
  
> Attribute des Verbs. 
    
 **ulFlags**
  
> Flag, das das Format des Anzeigenamens des Verbs angibt. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Der Anzeigename ist im Unicode-Format. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, ist der Anzeigename im ANSI-Format.
    
## <a name="remarks"></a>Bemerkungen

Die **SMAPIVerb** -Struktur wird als Parameter in den folgenden Methoden übergeben: 
  
- [IMAPIFormContainer::ResolveMultipleMessageClasses](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [IMAPIFormMgr::ResolveMultipleMessageClasses](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a>Siehe auch



[CbMessageClassArray](cbmessageclassarray.md)


[MAPI-Strukturen](mapi-structures.md)

