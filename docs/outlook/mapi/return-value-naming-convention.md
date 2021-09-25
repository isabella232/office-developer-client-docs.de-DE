---
title: Benennungskonvention für Rückgabewerte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 2c1cdd7b-82f1-46f2-a7ce-e0efe857b7cd
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 80d8b9e1f38422977ff327aac90830ed7b58a96b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624286"
---
# <a name="return-value-naming-convention"></a>Benennungskonvention für Rückgabewerte

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
The MAPICODE. Die H-Headerdatei enthält viele der Werte, die ein Client oder Dienstanbieter möglicherweise von einer Implementierung einer Schnittstellenmethode zurückgibt oder die von einem Aufruf zurückgegeben werden.
  
Die Codes zur Darstellung von Warnungs- und Fehlerbedingungen folgen einer anderen Benennungskonvention, die mit dem Präfix MAPI, einem Unterstrich und einem W oder E beginnt, um den Codetyp anzugeben. Der Rest des Codes ist eine kurze Zeichenfolge, um die Bedingung zu beschreiben. Jedes Wort in der Zeichenfolge wird durch einen Unterstrich getrennt. Beispielsweise gibt der Fehlerwert MAPI_E_TOO_COMPLEX an, dass die Implementierung nicht verarbeiten konnte, was im Aufruf angefordert wurde. Der Warnwert MAPI_W_PARTIAL_COMPLETION gibt an, dass der Aufruf erfolgreich war, es jedoch Probleme gab. Nur ein Teil des Vorgangs wurde erfolgreich abgeschlossen.
  

