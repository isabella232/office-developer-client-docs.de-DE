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
  
Die Benutzeroberfläche eines Formulars bietet in der Regel Menüelemente oder Steuerelemente, mit denen Benutzer eine Art von Aktion mit dem Formular ergreifen können. Es ist der Auftrag des Formularservers, diese Benutzeraktionen zu verarbeiten. Diese Schnittstelle wird mithilfe standardmäßiger Win32-APIs implementiert. Das Schreiben einer ist genauso wie das Schreiben anderer Schnittstellen für reguläre Win32-Programme.
  
Häufig sind Benutzeraktionen Verben zugeordnet. Ein Verb ist der Name einer Aktion, die für eine bestimmte Nachrichtenklasse spezifisch ist. Beispielsweise ist **Reply** ein Verb, das von vielen Formularservern implementiert wird, von denen jeder eine andere Interpretation dieses Verbs haben kann. Verben werden manchmal als Befehle bezeichnet. 
  
> [!NOTE]
> Nicht alle Menüelemente und Steuerelemente in einem Formular entsprechen einem Verb. Beispielsweise entspricht eine **Schaltfläche Abbrechen** nicht einem Cancel-Verb auf dem Formularserver. In der Regel werden Verben Aktionen zugeordnet, die für eine bestimmte Nachrichtenklasse oder eine Reihe von Nachrichtenklassen spezifisch sind. Obwohl verschiedene Nachrichtenklassen unterschiedliche Verben unterstützen können, unterstützen alle mindestens das Verb Open, das die Benutzeroberfläche des Formulars anzeigt und es mit den Eigenschaftswerten der Nachricht lädt. 
  
Verben können keine Parameter übernehmen. Formulare, die Befehle mit variablen Parametern exportieren, müssen die Automatisierungsmechanismen verwenden.
  
Clients können mithilfe der [IMAPIFormInfo::CalcVerbSet-Methode,](imapiforminfo-calcverbset.md) die vom MAPI-Formular-Manager implementiert wird, bestimmen, welche Verben von einer bestimmten Nachrichtenklasse unterstützt werden. Der Formular-Manager ruft diese Informationen aus der Konfigurationsdatei des Formulars ab. Der von dieser Methode zurückgegebene Verbsatz wird vom Client verwendet, um dem Benutzer anzuzeigen, welche Befehle für eine Nachricht ausgeführt werden können. Beispielsweise kann ein Client Benutzern das Klicken auf die rechte Maustaste über einer Nachricht ermöglichen, um Verben für diese Nachricht anzeigen zu können. 
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Formulare](mapi-forms.md)

