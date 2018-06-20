---
title: LOOKUP-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251457
localization_priority: Normal
ms.assetid: cb6ec664-6062-75d0-1514-8058b98c2c36
description: Gibt einen nullbasierten Index, der gibt die Position der Teilzeichenfolge Schlüssel in einer Liste oder gibt-1 zurück, wenn die Zielzeichenfolge das Trennzeichen enthält.
ms.openlocfilehash: e1fd433282871135d385d1c980c77041cd49cdf4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797423"
---
# <a name="lookup-function"></a>LOOKUP-Funktion

Gibt einen nullbasierten Index, der gibt die Position der Teilzeichenfolge _Schlüssel_ in einer _Liste_oder gibt-1 zurück, wenn die Zielzeichenfolge das _Trennzeichen_enthält.
  
## <a name="syntax"></a>Syntax

Nachschlagen ("** *Schlüssel* **","** *Liste* **"[,"** *Trennzeichen* **"]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Schlüssel_ <br/> |Erforderlich  <br/> |**String** <br/> |Die zu suchende Zeichenfolge.  <br/> |
| _list_ <br/> |Erforderlich  <br/> |**String** <br/> | Die Liste, in der gesucht werden soll.  <br/> |
| _delimiter_ <br/> |Optional  <br/> |**String** <br/> | Die Zeichenfolge an, in der _Liste_als Trennzeichen verwendet. Zeichenfolge für ein _Trennzeichen_ kann mehr als ein Zeichen lang sein und kann multibyte-Zeichen enthalten. Der Standardwert ist eine durch Semikolons.  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

Numeric
  
## <a name="remarks"></a>Bemerkungen

Die LOOKUP-Funktion verwendet eine Suche, die nicht zwischen Klein- und Großschreibung unterscheidet. Ist der Liste ein Trennzeichen voran- bzw. nachgestellt, wird eine leere Zeichenfolge vor bzw. hinter der Liste unterstellt. Aufeinander folgende Trennzeichen implizieren eine eingefügte leere Zeichenfolge. 
  
Sämtliche Argumente müssen Zeichenfolgen oder in Zeichenfolgen konvertierbare Ausdrücke sein. Ist dies nicht der Fall, wird eine leere Zeichenfolge für das fehlerhafte Argument verwendet. 
  
## <a name="example-1"></a>Beispiel 1

LOOKUP("Ratte","Katze;Ratte;;Ziege")
  
Gibt 1 zurück.
  
## <a name="example-2"></a>Beispiel 2

LOOKUP("",";Katze;Ratte;;Ziege")
  
Gibt 0 zurück.
  
## <a name="example-3"></a>Beispiel 3

LOOKUP("t","Katze;Ratte;;Ziege","a")
  
Gibt 3 zurück.
  

