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
description: Gibt einen nullbasierten Index zurück, der die Position des Schlüssels der Teilzeichenfolge in einer Liste angibt, oder gibt-1 zurück, wenn die Zielzeichenfolge das Trennzeichen enthält.
ms.openlocfilehash: 10fc32e6e979ab819246161dedfb1183c2683a99
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410329"
---
# <a name="lookup-function"></a>LOOKUP Function

Gibt einen nullbasierten Index zurück, der die Position des _Schlüssels_ der Teilzeichenfolge in einer _Liste_angibt, oder gibt-1 zurück, wenn die Zielzeichenfolge das _Trenn_Zeichen enthält.
  
## <a name="syntax"></a>Syntax

Lookup ("* * *Key* * *", "* * *Liste* * *" [, "* * *Trennzeichen* * *"]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _key_ <br/> |Erforderlich  <br/> |**String** <br/> |Die zu suchende Zeichenfolge.  <br/> |
| _list_ <br/> |Erforderlich  <br/> |**String** <br/> | Die Liste, in der gesucht werden soll.  <br/> |
| _delimiter_ <br/> |Optional  <br/> |**String** <br/> | Die zu verwendende Zeichenfolge in _List_. Eine _Trenn_ Zeichen Zeichenfolge kann mehr als ein Zeichen lang sein und Multibyte-Zeichen enthalten. Das Standardtrennzeichen ist ein Semikolon.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Numeric
  
## <a name="remarks"></a>Bemerkungen

Die LOOKUP-Funktion verwendet eine Suche, die nicht zwischen Klein- und Großschreibung unterscheidet. Ist der Liste ein Trennzeichen voran- bzw. nachgestellt, wird eine leere Zeichenfolge vor bzw. hinter der Liste unterstellt. Aufeinander folgende Trennzeichen implizieren eine eingefügte leere Zeichenfolge. 
  
Sämtliche Argumente müssen Zeichenfolgen oder in Zeichenfolgen konvertierbare Ausdrücke sein. Ist dies nicht der Fall, wird eine leere Zeichenfolge für das fehlerhafte Argument verwendet. 
  
## <a name="example-1"></a>Beispiel 1

LOOKUP ("Rat", "Cat; Rat;; Ziege ")
  
Gibt 1 zurück.
  
## <a name="example-2"></a>Beispiel 2

LOOKUP ("", "; Cat; Rat;; Ziege ")
  
Gibt 0 zurück.
  
## <a name="example-3"></a>Beispiel 3

LOOKUP ("t", "Cat; Rat;; Ziege "," a ")
  
Gibt 3 zurück.
  

