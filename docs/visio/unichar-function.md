---
title: UNICHAR-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60117
localization_priority: Normal
ms.assetid: 371a475d-50f7-6b4c-4b47-581cd778dcba
description: Gibt das Unicode-Zeichen aus einer Zahl zurück.
ms.openlocfilehash: 81e76b72da35f79dee9ad6afbde51bc2e228483c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417581"
---
# <a name="unichar-function"></a>UNICHAR Function

Gibt das Unicode-Zeichen aus einer Zahl zurück. 
  
## <a name="syntax"></a>Syntax

UnCHAR (* * *Number* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Anzahl_ <br/> |Erforderlich  <br/> |**Integer** <br/> |Eine ganze Zahl zwischen 1 und 65.535 (einschließlich); andernfalls gibt die Funktion einen Fehler zurück.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die resultierende Zeichenfolge hat eine Länge von einem Unicode-Zeichen (zwei Zeichen). 
  
## <a name="example"></a>Beispiel

UNCHAR (65) 
  
Gibt einen (lateinischen Großbuchstaben A) zurück. 
  

