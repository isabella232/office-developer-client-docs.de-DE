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
description: Gibt das Unicode-Zeichen einer Zahl zurück.
ms.openlocfilehash: 06f97717ee4d5965253b0da7cfd5c35faf0ca2f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798350"
---
# <a name="unichar-function"></a>UNICHAR Function

Gibt das Unicode-Zeichen einer Zahl zurück. 
  
## <a name="syntax"></a>Syntax

UNICHAR (** *Anzahl* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Anzahl_ <br/> |Erforderlich  <br/> |**Integer** <br/> |Eine ganze Zahl zwischen 1 und 65.535 (einschließlich); andernfalls gibt die Funktion einen Fehler zurück.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die resultierende Zeichenfolge hat eine Länge von einem Unicode-Zeichen (zwei Zeichen). 
  
## <a name="example"></a>Beispiel

UNICHAR(65) 
  
Gibt ein (lateinischen Großbuchstaben A) 
  

