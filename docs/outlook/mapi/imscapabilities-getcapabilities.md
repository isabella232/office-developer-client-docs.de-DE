---
title: IMSCapabilitiesGetCapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSCapabilities.GetCapabilities
api_type:
- COM
ms.assetid: c77a8ef1-0730-d458-b35f-451d3f450fac
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b76c55fd9ddc3aa7698f75aa6ce965544b2c9aae
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409258"
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
  
> [in] Auswahl, die angibt, welche Funktionen zurückzukehren sind.
    
## <a name="return-value"></a>Rückgabewert

MSCAP_SECURE_FOLDER_HOMEPAGES
  
> Unterstützung für Ordnerhomepages in einem nicht standardmäßigen Speicher. Dies kann zurückgegeben werden, **wenn MSCAP_SEL_FOLDER** in *mscapSelector angegeben ist.* 
    
MSCAP_RES_ANNOTATION
  
> Wenn eine Einschränkung ungültige Argumente wie ungültige Eigenschaften enthält, ignoriert der Speicher die ungültigen Argumente und verarbeitet nur die gültigen Argumente. Dies kann zurückgegeben werden, **MSCAP_SEL_RESTRICTION** in *mscapSelector angegeben ist.* 
    
NULL
  
> Der Speicher unterstützt keine Funktionen basierend auf dem angegebenen Selektor.
    

