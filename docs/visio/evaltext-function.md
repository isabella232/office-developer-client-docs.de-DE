---
title: EVALTEXT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251422
localization_priority: Normal
ms.assetid: c9b5b96c-d8c8-6119-e3f1-a2ce9d7c043e
description: Wertet den Text in Shapename wie eine Formel aus und gibt das Ergebnis zurück.
ms.openlocfilehash: 69e79a23faa9d09aa2ad51f83363064b54742152
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796950"
---
# <a name="evaltext-function"></a>EVALTEXT-Funktion

Wertet den Text in _Shapename_ wie eine Formel aus und gibt das Ergebnis zurück. 
  
## <a name="syntax"></a>Syntax

EVALTEXT (** *Shapename! TheText* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Shapename! TheText_ <br/> |Erforderlich  <br/> |**String** <br/> |Eine Zelle, die bei Änderungen an der Textgestaltung des zugeordneten Shapes ausgelöst wird.  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

String
  
## <a name="remarks"></a>Hinweise

 _Shapename_ kann verwendet werden, um auf den Text eines Shapes als das aktuelle Shape zu verweisen. 
  
Wenn kein Text vorhanden ist, ist das Ergebnis 0. Wenn der Text nicht ausgewertet werden kann, gibt die Funktion einen Fehler zurück.
  
## <a name="example"></a>Beispiel

EVALTEXT(Line.2!theText) 
  
Wertet den Text des Shapes Line.2 aus. Wenn Line.2 beispielsweise den Text "4 ft + 0,5 ft" enthält, wird der Wert 4,5 ft zurückgegeben. 
  

