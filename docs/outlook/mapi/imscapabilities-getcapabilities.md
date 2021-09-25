---
title: IMSCapabilitiesGetCapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMSCapabilities.GetCapabilities
api_type:
- COM
ms.assetid: c77a8ef1-0730-d458-b35f-451d3f450fac
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b4f0b47aa1c8f79db886a0eba5f146404fd9031b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630537"
---
# <a name="imscapabilitiesgetcapabilities"></a>IMSCapabilities::GetCapabilities

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ruft Informationen dazu ab, was ein Speicher basierend auf dem angegebenen Selektor unterstützen kann.
  
```cpp
ULONG GetCapabilities( 
MSCAP_SELECTOR mscapSelector 
);
```

## <a name="parameters"></a>Parameter

 *mscapSelector* 
  
> [in] Auswahl, die angibt, welche Funktionen zurückgegeben werden sollen.
    
## <a name="return-value"></a>Rückgabewert

MSCAP_SECURE_FOLDER_HOMEPAGES
  
> Unterstützung für Ordner-Homepages in einem nicht standardmäßigen Speicher. Dies kann zurückgegeben werden, wenn **MSCAP_SEL_FOLDER** in  *mscapSelector*  angegeben ist. 
    
MSCAP_RES_ANNOTATION
  
> Wenn eine Einschränkung ungültige Argumente enthält, z. B. ungültige Eigenschaften, ignoriert der Speicher die ungültigen Argumente und verarbeitet nur die gültigen Argumente. Dies kann zurückgegeben werden, wenn **MSCAP_SEL_RESTRICTION** in  *mscapSelector*  angegeben ist. 
    
NULL
  
> Der Speicher unterstützt keine Funktion basierend auf der angegebenen Auswahl.
    

