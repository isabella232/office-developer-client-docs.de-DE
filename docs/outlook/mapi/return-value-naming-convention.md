---
title: BeNennungsKonvention für Rückgabewerte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2c1cdd7b-82f1-46f2-a7ce-e0efe857b7cd
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6786e1ca901215abd709a11401c3026d62c6ffc8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279825"
---
# <a name="return-value-naming-convention"></a>BeNennungsKonvention für Rückgabewerte

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die MAPICODE. H-Headerdatei enthält viele der Werte, die ein Client oder Dienstanbieter von einer Implementierung der Schnittstellenmethode zurückgeben kann oder von einem Aufruf zurückgegeben wird.
  
Die Codes zur Darstellung von Warnungs-und Fehlerbedingungen befolgen eine andere Benennungskonvention, die mit dem Präfix MAPI, einem Unterstrich und einem W-oder E-Wert beginnt, um den Typ des Codes anzugeben. Der Rest des Codes ist eine kurze Zeichenfolge zur Beschreibung der Bedingung. Jedes Wort in der Zeichenfolge wird durch einen Unterstrich getrennt. Der Fehlerwert MAPI_E_TOO_COMPLEX gibt beispielsweise an, dass die Implementierung nicht verarbeiten konnte, was im Aufruf angefordert wurde. Der Warnungswert MAPI_W_PARTIAL_COMPLETION gibt an, dass der Aufruf erfolgreich war, aber Probleme aufgetreten sind. Nur ein Teil des Vorgangs wurde erfolgreich abgeschlossen.
  

