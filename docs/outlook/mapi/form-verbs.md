---
title: Formular Verben
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a63bf0a7-24e6-4eef-98e8-3744ce5f9f2d
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1ecc80feec2b0a86f35d03f1ca4f75ea9ff094e4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791723"
---
# <a name="form-verbs"></a>Formular Verben

**Betrifft**: Outlook 
  
Benutzeroberfläche des Formulars bietet in der Regel Menüelemente oder Steuerelemente, mit denen Benutzer die verschiedenste Aktion mit dem Formular. Es ist dem Formular Server Auftrag an diese Benutzeraktionen zu behandeln. Diese Schnittstelle wird mit standard Win32-APIs implementiert. Schreiben einer verhält sich wie andere Schnittstellen für regulären Win32-Programme schreiben.
  
Oft sind Benutzeraktionen Verben zugeordnet. Ein Verb ist der Name für eine Aktion, die speziell für eine bestimmte Nachrichtenklasse ist. Beispielsweise ist **Antwort** ein Verb, die jeweils eine unterschiedliche Interpretation von diesem Verb möglicherweise viele Formular Server implementiert wird. Verben werden manchmal als Befehle bezeichnet. 
  
> [!NOTE]
> Nicht alle Menüelemente und Steuerelemente eines Formulars entsprechen ein Verb. Beispielsweise entspricht eine Schaltfläche **Abbrechen** nicht abbrechen Verb innerhalb des Servers Formular. In der Regel Verben, die Aktionen, die speziell für eine bestimmte Nachrichtenklasse oder eine Gruppe von Nachrichtenklassen zugeordnet sind. Obwohl unterschiedliche Nachrichtenklassen verschiedene Sätze von Verben unterstützen können, unterstützen das Open Verb, das Benutzeroberfläche des Formulars angezeigt und lädt ihn mit der Nachricht Eigenschaftswerte mindestens. 
  
Verben können keine Parameter verwendet werden. Formulare, die Befehle mit Variable Parameter exportieren müssen die Automatisierung Mechanismen verwenden.
  
Clients können ermitteln, welche Verben von einer bestimmten Nachrichtenklasse über die Methode [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md) unterstützt werden die von der MAPI-Formular-Manager implementiert wird. Der Formular-Manager ruft diese Informationen aus der Konfigurationsdatei des Formulars ab. Der Verb Satz von dieser Methode zurückgegebene wird vom Client verwendet, um dem Benutzer anzuzeigen, welche Befehle für eine Nachricht ausgeführt werden können. Beispielsweise kann ein Client Benutzer über eine Meldung an Verben für die Nachricht der rechten Maustaste auf aktivieren. 
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Formulare](mapi-forms.md)

