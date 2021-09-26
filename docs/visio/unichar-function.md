---
title: UNICHAR-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60117
ms.localizationpriority: medium
ms.assetid: 371a475d-50f7-6b4c-4b47-581cd778dcba
description: Gibt das Unicode-Zeichen aus einer Zahl zurück.
ms.openlocfilehash: 8f37e4890b785a0b3557efc1167dc80868f72c7a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603221"
---
# <a name="unichar-function"></a>UNICHAR Function

Gibt das Unicode-Zeichen aus einer Zahl zurück. 
  
## <a name="syntax"></a>Syntax

UNICHAR (** *Zahl* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Anzahl_ <br/> |Erforderlich  <br/> |**Integer** <br/> |Eine ganze Zahl zwischen 1 und 65.535 (einschließlich); andernfalls gibt die Funktion einen Fehler zurück.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Die resultierende Zeichenfolge hat eine Länge von einem Unicode-Zeichen (zwei Zeichen). 
  
## <a name="example"></a>Beispiel

UNICHAR(65) 
  
Gibt A zurück (lateinische Großbuchstaben A) 
  

