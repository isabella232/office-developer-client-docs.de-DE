---
title: ISocialProfileAreFriendsOrColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a0b586cd-65f6-4792-851c-4d36eaeec56d
description: Bestimmt, ob die angegebenen Benutzer Freunde sind.
ms.openlocfilehash: 183e47bea70ed378947afb6a1d0e5561fb9307f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412562"
---
# <a name="isocialprofilearefriendsorcolleagues"></a>ISocialProfile::AreFriendsOrColleagues

Bestimmt, ob die angegebenen Benutzer Freunde sind.
  
```cpp
HRESULT _stdcall AreFriendsOrColleagues(SAFEARRAY(BSTR) userIds, [out, retval] SAFEARRAY(VARIANT_BOOL)* results);
```

## <a name="parameters"></a>Parameter

_UserIds_
  
> [in] Eine Struktur, die ein Array von Benutzer-ID-Werten angibt, die einer Gruppe von Personen im sozialen Netzwerk entsprechen.
    
_ergebnisse_
  
> [out] Ein Zeiger auf die Struktur, der ein Array von booleschen Werten angibt, der angibt, ob die entsprechende Person im  _userIds-Array_ ein Freund ist. 
    
## <a name="remarks"></a>Hinweise

Für jede Person, die im Eingabearray des  _parameters userIds_ dargestellt wird, legt diese Methode das entsprechende Element im Ausgabearray des  _Results-Parameters_ fest. **true** gibt an, dass es sich bei der Person um einen Freund handelt, und **false** gibt an, dass es sich bei der Person nicht um einen Freund handelt. 
  
## <a name="see-also"></a>Siehe auch

- [ISocialProfile : ISocialPerson](isocialprofileisocialperson.md)

