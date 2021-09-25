---
title: Formularverben
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: a63bf0a7-24e6-4eef-98e8-3744ce5f9f2d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: bdad3d3f1bf09e46cf82db00f5201ee5c928e29d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59587972"
---
# <a name="form-verbs"></a>Formularverben

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Benutzeroberfläche eines Formulars bietet in der Regel Menüelemente oder Steuerelemente, mit denen Benutzer eine Art von Aktion mit dem Formular ausführen können. Es ist der Auftrag des Formularservers, diese Benutzeraktionen zu verarbeiten. Diese Schnittstelle wird mit win32-Standard-APIs implementiert. Das Schreiben einer schnittstelle entspricht dem Schreiben anderer Schnittstellen für reguläre Win32-Programme.
  
Häufig sind Benutzeraktionen Verben zugeordnet. Ein Verb ist der Name einer Aktion, die für eine bestimmte Nachrichtenklasse spezifisch ist. Beispielsweise ist **Reply** ein Verb, das von vielen Formularservern implementiert wird, von denen jeder eine andere Interpretation dieses Verbs haben kann. Verben werden manchmal als Befehle bezeichnet. 
  
> [!NOTE]
> Nicht alle Menüelemente und Steuerelemente in einem Formular entsprechen einem Verb. Eine Schaltfläche  Abbrechen entspricht z. B. keinem Cancel-Verb auf dem Formularserver. In der Regel sind Verben Aktionen zugeordnet, die für eine bestimmte Nachrichtenklasse oder eine Reihe von Nachrichtenklassen spezifisch sind. Obwohl unterschiedliche Nachrichtenklassen unterschiedliche Verbsätze unterstützen können, unterstützen alle mindestens das Open-Verb, das die Benutzeroberfläche des Formulars anzeigt und mit den Eigenschaftswerten der Nachricht lädt. 
  
Verben dürfen keine Parameter verwenden. Formulare, die Befehle mit variablen Parametern exportieren, müssen die Automatisierungsmechanismen verwenden.
  
Clients können bestimmen, welche Verben von einer bestimmten Nachrichtenklasse unterstützt werden, indem sie die [IMAPIFormInfo::CalcVerbSet-Methode](imapiforminfo-calcverbset.md) verwenden, die vom MAPI-Formular-Manager implementiert wird. Der Formular-Manager ruft diese Informationen aus der Konfigurationsdatei des Formulars ab. Das von dieser Methode zurückgegebene Verb wird vom Client verwendet, um dem Benutzer anzuzeigen, welche Befehle für eine Nachricht ausgeführt werden können. Mit einem Client können Benutzer beispielsweise mit der rechten Maustaste auf eine Nachricht klicken, um verben anzuzeigen, die für diese Nachricht gelten. 
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Formulare](mapi-forms.md)

