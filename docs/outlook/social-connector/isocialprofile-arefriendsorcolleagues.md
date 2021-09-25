---
title: ISocialProfileAreFriendsOrColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: a0b586cd-65f6-4792-851c-4d36eaeec56d
description: Bestimmt, ob die angegebenen Benutzer Freunde sind.
ms.openlocfilehash: 5f782e998f46485cc5560e13ffbe55394702dbc2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563217"
---
# <a name="isocialprofilearefriendsorcolleagues"></a>ISocialProfile::AreFriendsOrColleagues

Bestimmt, ob die angegebenen Benutzer Freunde sind.
  
```cpp
HRESULT _stdcall AreFriendsOrColleagues(SAFEARRAY(BSTR) userIds, [out, retval] SAFEARRAY(VARIANT_BOOL)* results);
```

## <a name="parameters"></a>Parameter

_UserIds_
  
> [in] Eine Struktur, die ein Array von Benutzer-ID-Werten angibt, die einer Gruppe von Personen im sozialen Netzwerk entsprechen.
    
_Ergebnisse_
  
> [out] Ein Zeiger auf eine Struktur, der ein Array von booleschen Werten angibt, der angibt, ob die entsprechende Person im  _UserIds-Array_ ein Freund ist. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Für jede Person, die im Eingabearray des  _parameters userIds_ dargestellt wird, legt diese Methode das entsprechende Element im Ausgabearray des  _Ergebnisparameters_ fest. **"true"** gibt an, dass die Person ein Freund ist, und **"false"** gibt an, dass die Person kein Freund ist. 
  
## <a name="see-also"></a>Siehe auch

- [ISocialProfile : ISocialPerson](isocialprofileisocialperson.md)

