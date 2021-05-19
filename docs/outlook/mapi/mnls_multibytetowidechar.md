---
title: MNLS_MultiByteToWideChar
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 065d78bf-4c9c-48dd-b1f1-b4e59f3f1243
description: 'Letzte Änderung: 21. Februar 2012'
ms.openlocfilehash: 1f137aba40703fe84e5753ee6e370262f780f0a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338241"
---
# <a name="mnls_multibytetowidechar"></a>MNLS_MultiByteToWideChar

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ähnlich wie **MultiByteToWideChar**, das eine Zeichenzeichenfolge einer UTF-16-Zeichenfolge (breite Zeichen) zu ordnet. Die Zeichenzeichenfolge ist nicht unbedingt aus einem Mehrbyte-Zeichensatz.
  
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
  
> [in] Codeseite, die beim Ausführen der Konvertierung verwendet werden soll.
    
 _dwFlags_
  
> [in] Flags, die den Konvertierungstyp angeben.
    
 _lpMultiByteStr_
  
> [in] Zeiger auf die zu konvertierende Zeichenzeichenfolge.
    
 _cchMultiByte_
  
> [in] Größe der vom  _lpMultiByteStr-Parameter_ angegebenen Zeichenfolge in Bytes. 
    
 _lpWideCharStr_
  
> [out] Optional. Zeiger auf einen Puffer, der die konvertierte Zeichenfolge empfängt.
    
 _cchWideChar_
  
> [in] Größe (in Zeichen) des Puffers, der durch _lpWideCharStr angegeben wird._
    
## <a name="return-value"></a>Rückgabewert

Gibt die Anzahl der Zeichen zurück, die in den puffer geschrieben werden, der von  _lpWideCharStr_ angegeben wird, wenn dies erfolgreich ist. 
  
## <a name="remarks"></a>Hinweise

Diese Funktion umschließt die **MultiByteToWideChar-Funktion.** Weitere Informationen finden Sie unter [MultiByteToWideChar](https://msdn.microsoft.com/library/dd319072%28VS.85%29.aspx).
  

