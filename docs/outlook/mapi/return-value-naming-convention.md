---
title: Rückgabewertbenennungskonvention
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2c1cdd7b-82f1-46f2-a7ce-e0efe857b7cd
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6786e1ca901215abd709a11401c3026d62c6ffc8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423615"
---
# <a name="return-value-naming-convention"></a>Rückgabewertbenennungskonvention

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der MAPICODE. Die H-Headerdatei enthält viele der Werte, die ein Client oder Dienstanbieter von einer Schnittstellenmethodesimplementierung zurückgeben kann oder von einem Aufruf zurückgegeben wird.
  
Die Codes, die Warnungs- und Fehlerbedingungen darstellen sollen, folgen einer anderen Benennungskonvention, die mit dem Präfix MAPI, einem Unterstrich und entweder einem W oder einem E beginnt, um den Codetyp anzugeben. Der Rest des Codes ist eine kurze Zeichenfolge, um die Bedingung zu beschreiben. Jedes Wort in der Zeichenfolge wird durch einen Unterstrich getrennt. Beispielsweise gibt der Fehlerwert MAPI_E_TOO_COMPLEX an, dass die Implementierung nicht verarbeiten konnte, was im Aufruf angefordert wurde. Der Warnwert MAPI_W_PARTIAL_COMPLETION an, dass der Aufruf erfolgreich war, es aber Probleme gab. Nur ein Teil des Vorgangs wurde erfolgreich abgeschlossen.
  

