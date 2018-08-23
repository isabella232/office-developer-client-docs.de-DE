---
title: Rückgabewert-Benennungskonvention
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2c1cdd7b-82f1-46f2-a7ce-e0efe857b7cd
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4d7a95e4681370e1aaf4f8b4c4b7ca0814b3aae7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581846"
---
# <a name="return-value-naming-convention"></a>Rückgabewert-Benennungskonvention

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Die MAPICODE. H-Headerdatei enthält viele der Werte, die ein Client oder Dienstanbieter zurückgeben vom eine Implementierung-Methode oder möglicherweise von einem Aufruf zurückgegebene angezeigt.
  
Die Codes zur Darstellung von Warnungen und Fehler Bedingungen führen Sie eine unterschiedliche Benennungskonvention, die mit dem Präfix MAPI, einem Unterstrich und entweder ein W oder einer E an, dass der Typ des Codes beginnt. Der Rest des Codes ist eine kurze Zeichenfolge, um die Bedingung zu beschreiben. Jedes Wort in der Zeichenfolge wird durch einen Unterstrich getrennt. Der Fehlerwert MAPI_E_TOO_COMPLEX gibt beispielsweise an, dass die Implementierung nicht verarbeiten kann den Inhalt in den Anruf angefordert wurde. Schwellenwert für die Warnung MAPI_W_PARTIAL_COMPLETION gibt an, dass der Aufruf war erfolgreich, aber ein Problem aufgetreten. Nur einen Teil der Vorgang wurde erfolgreich abgeschlossen.
  

