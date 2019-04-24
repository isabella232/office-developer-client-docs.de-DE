---
title: MNLS_MultiByteToWideChar
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 065d78bf-4c9c-48dd-b1f1-b4e59f3f1243
description: 'Zuletzt geändert: 21, 2012'
ms.openlocfilehash: 1f137aba40703fe84e5753ee6e370262f780f0a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338241"
---
# <a name="mnlsmultibytetowidechar"></a>MNLS_MultiByteToWideChar

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ähnlich wie **MultiByteToWideChar**wird eine zeichenFOLGE einer UTF-16-Zeichenfolge zugeordnet. Die Zeichenfolge ist nicht unbedingt aus einem Mehrbyte-Zeichensatz.
  
```cpp
int MNLS_MultiByteToWideChar(
  UINT uCodePage,
  DWORD dwFlags,
  LPCSTR lpMultiByteStr,
  int cchMultiByte,
  LPWSTR lpWideCharStr,
  int cchWideChar);
```

## <a name="parameters"></a>Parameter

 _uCodePage_
  
> in Codepage, die beim Ausführen der Konvertierung verwendet werden soll.
    
 _dwFlags_
  
> in Flags, die den Konvertierungs angeben.
    
 _lpMultiByteStr_
  
> in Zeiger auf die Zeichenfolge, die konvertiert werden soll.
    
 _cchMultiByte_
  
> in Größe (in Bytes) der vom _lpMultiByteStr_ -Parameter angegebenen Zeichenfolge. 
    
 _lpWideCharStr_
  
> [out] Optional. Zeiger auf einen Puffer, der die konvertierte Zeichenfolge empfängt.
    
 _cchWideChar_
  
> in Die Größe des von _lpWideCharStr_angegebenen Puffers in Zeichen.
    
## <a name="return-value"></a>Rückgabewert

Gibt die Anzahl von Zeichen zurück, die in den von _lpWideCharStr_ angegebenen Puffer geschrieben werden, falls erfolgreich. 
  
## <a name="remarks"></a>Bemerkungen

Diese Funktion umschließt die **MultiByteToWideChar** -Funktion. Weitere Informationen finden Sie unter [MultiByteToWideChar](https://msdn.microsoft.com/library/dd319072%28VS.85%29.aspx).
  

