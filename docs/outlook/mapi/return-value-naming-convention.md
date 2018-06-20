---
title: Rückgabewert Benennungskonvention
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2c1cdd7b-82f1-46f2-a7ce-e0efe857b7cd
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 990a48c661621a3a704236a850f5d09239a12fca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795406"
---
# <a name="return-value-naming-convention"></a>Rückgabewert Benennungskonvention

  
  
**Betrifft**: Outlook 
  
Die MAPICODE. H-Headerdatei enthält viele der Werte, die ein Client oder Dienstanbieter zurückgeben vom eine Implementierung-Methode oder möglicherweise von einem Aufruf zurückgegebene angezeigt.
  
Die Codes zur Darstellung von Warnungen und Fehler Bedingungen führen Sie eine unterschiedliche Benennungskonvention, die mit dem Präfix MAPI, einem Unterstrich und entweder ein W oder einer E an, dass der Typ des Codes beginnt. Der Rest des Codes ist eine kurze Zeichenfolge, um die Bedingung zu beschreiben. Jedes Wort in der Zeichenfolge wird durch einen Unterstrich getrennt. Der Fehlerwert MAPI_E_TOO_COMPLEX gibt beispielsweise an, dass die Implementierung nicht verarbeiten kann den Inhalt in den Anruf angefordert wurde. Schwellenwert für die Warnung MAPI_W_PARTIAL_COMPLETION gibt an, dass der Aufruf war erfolgreich, aber ein Problem aufgetreten. Nur einen Teil der Vorgang wurde erfolgreich abgeschlossen.
  

