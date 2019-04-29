---
title: Formularverben
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a63bf0a7-24e6-4eef-98e8-3744ce5f9f2d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: dbd08437dfdd38c3a43cbf12eae8710cc8e3661e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424028"
---
# <a name="form-verbs"></a>Formularverben

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Benutzeroberfläche eines Formulars bietet normalerweise Menüelemente oder Steuerelemente, mit denen Benutzer eine Art von Aktion mit dem Formular ausführen können. Diese Benutzeraktionen werden vom Formularserver ausgeführt. Diese Schnittstelle wird mit standardmäßigen Win32-APIs implementiert; Writing One ist genau wie das Schreiben von anderen Schnittstellen für reguläre Win32-Programme.
  
Häufig werden Benutzeraktionen mit Verben verknüpft. Ein Verb ist der Name für eine Aktion, die für eine bestimmte Nachrichtenklasse spezifisch ist. **Reply** ist beispielsweise ein Verb, das von vielen Formular Servern implementiert wird, von denen jede eine andere Interpretation dieses Verbs haben kann. Verben werden manchmal auch als Befehle bezeichnet. 
  
> [!NOTE]
> Nicht alle Menüelemente und Steuerelemente in einem Formular entsprechen einem Verb. Beispielsweise entspricht eine **Abbrechen** -Schaltfläche nicht einem Abbrechen-Verb innerhalb des Formular Servers. Verben sind in der Regelaktionen zugeordnet, die spezifisch für eine bestimmte Nachrichtenklasse oder eine Gruppe von Nachrichtenklassen sind. Obwohl unterschiedliche Nachrichtenklassen unterschiedliche Verben unterstützen können, unterstützen alle mindestens das offene Verb, das die Benutzeroberfläche des Formulars anzeigt und mit den Eigenschaftenwerten der Nachricht lädt. 
  
Verben können keine Parameter annehmen. Formulare, die Befehle mit Variablen Parametern exportieren, müssen die Automatisierungsmechanismen verwenden.
  
Clients können mithilfe der [IMAPIFormInfo:: CalcVerbSet](imapiforminfo-calcverbset.md) -Methode, die vom MAPI-Formular-Manager implementiert wird, bestimmen, welche Verben von einer bestimmten Nachrichtenklasse unterstützt werden. Der Formular-Manager ruft diese Informationen aus der Konfigurationsdatei des Formulars ab. Das von dieser Methode zurückgegebene Verb Set wird vom Client verwendet, um den Benutzer anzuzeigen, welche Befehle für eine Nachricht ausgeführt werden können. Beispielsweise kann ein Client Benutzern ermöglichen, mit der rechten Maustaste auf eine Nachricht zu klicken, um Verben anzuzeigen, die für diese Nachricht gelten. 
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Formulare](mapi-forms.md)

