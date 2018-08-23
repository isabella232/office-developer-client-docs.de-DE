---
title: Formular Verben
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a63bf0a7-24e6-4eef-98e8-3744ce5f9f2d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 27999c141fdeb3e1610213db128bc4ad3d049e6d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594103"
---
# <a name="form-verbs"></a>Formular Verben

**Betrifft**: Outlook 2013 | Outlook 2016 
  
Benutzeroberfläche des Formulars bietet in der Regel Menüelemente oder Steuerelemente, mit denen Benutzer die verschiedenste Aktion mit dem Formular. Es ist dem Formular Server Auftrag an diese Benutzeraktionen zu behandeln. Diese Schnittstelle wird mit standard Win32-APIs implementiert. Schreiben einer verhält sich wie andere Schnittstellen für regulären Win32-Programme schreiben.
  
Oft sind Benutzeraktionen Verben zugeordnet. Ein Verb ist der Name für eine Aktion, die speziell für eine bestimmte Nachrichtenklasse ist. Beispielsweise ist **Antwort** ein Verb, die jeweils eine unterschiedliche Interpretation von diesem Verb möglicherweise viele Formular Server implementiert wird. Verben werden manchmal als Befehle bezeichnet. 
  
> [!NOTE]
> Nicht alle Menüelemente und Steuerelemente eines Formulars entsprechen ein Verb. Beispielsweise entspricht eine Schaltfläche **Abbrechen** nicht abbrechen Verb innerhalb des Servers Formular. In der Regel Verben, die Aktionen, die speziell für eine bestimmte Nachrichtenklasse oder eine Gruppe von Nachrichtenklassen zugeordnet sind. Obwohl unterschiedliche Nachrichtenklassen verschiedene Sätze von Verben unterstützen können, unterstützen das Open Verb, das Benutzeroberfläche des Formulars angezeigt und lädt ihn mit der Nachricht Eigenschaftswerte mindestens. 
  
Verben können keine Parameter verwendet werden. Formulare, die Befehle mit Variable Parameter exportieren müssen die Automatisierung Mechanismen verwenden.
  
Clients können ermitteln, welche Verben von einer bestimmten Nachrichtenklasse über die Methode [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md) unterstützt werden die von der MAPI-Formular-Manager implementiert wird. Der Formular-Manager ruft diese Informationen aus der Konfigurationsdatei des Formulars ab. Der Verb Satz von dieser Methode zurückgegebene wird vom Client verwendet, um dem Benutzer anzuzeigen, welche Befehle für eine Nachricht ausgeführt werden können. Beispielsweise kann ein Client Benutzer über eine Meldung an Verben für die Nachricht der rechten Maustaste auf aktivieren. 
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Formulare](mapi-forms.md)

