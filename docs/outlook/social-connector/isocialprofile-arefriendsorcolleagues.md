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
ms.openlocfilehash: 17e7864dc60bf99df2028e5f6c57f0619d880a8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795968"
---
# <a name="isocialprofilearefriendsorcolleagues"></a>ISocialProfile::AreFriendsOrColleagues

Bestimmt, ob die angegebenen Benutzer Freunde sind.
  
```cpp
HRESULT _stdcall AreFriendsOrColleagues(SAFEARRAY(BSTR) userIds, [out, retval] SAFEARRAY(VARIANT_BOOL)* results);
```

## <a name="parameters"></a>Parameter

_Benutzer-IDs_
  
> [in] Eine Struktur, die ein Array von Benutzer-ID-Werte gibt an, die eine Gruppe von Personen im sozialen Netzwerk entsprechen.
    
_Ergebnisse_
  
> [out] Ein Zeiger auf die Struktur, die ein Array von boolesche Werte zurück, der angibt, ob die entsprechende Person in das Array _Benutzer-IDs_ ein Freund ist angibt. 
    
## <a name="remarks"></a>Hinweise

Für jede Person in der Eingabe der Parameter _UserIds_ gibt-Array dargestellt legt diese Methode das entsprechende Element in der Matrix des Parameters _Ergebnisse_ . **true** gibt an, dass die Person einen Freund, und **false** gibt an, dass die Person keinen Freund ist. 
  
## <a name="see-also"></a>Siehe auch

- [ISocialProfile: ISocialPerson](isocialprofileisocialperson.md)

