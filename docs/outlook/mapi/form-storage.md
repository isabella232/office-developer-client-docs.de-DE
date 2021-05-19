---
title: Formularspeicher
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6ddf9158-3c10-408a-aeaf-5a382c4339e7
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 793a34b093ba69f73be7e186bec0a769584bbac4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414893"
---
# <a name="form-storage"></a>Formularspeicher

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Obwohl es nicht erforderlich ist, alle Details zur physischen Speicherung von Formularen zu kennen, ist es hilfreich, einige der wichtigsten Konzepte zu verstehen. Daher bietet dieses Thema vor der Beschreibung der drei Typen von Formularbibliotheken, die vom Standardformular-Manager unterstützt werden, eine Übersicht über die Art und Weise, wie Formulare gespeichert werden.
  
Formulardefinitionen können physisch in Ordnern in einem oder mehreren MAPI-Nachrichtenspeichern gespeichert werden. Jeder MAPI-Ordner kann als zwei Bereiche zum Speichern von Nachrichtenobjekten bezeichnet werden: den Standardteil und den zugeordneten Teil. Der Standardteil des Ordners umfasst die Nachrichten und Ordner, die Benutzer bearbeiten.
  
Der zugeordnete Teil enthält ausgeblendete Nachrichtenobjekte, die dem Ordner zugeordnet sind, einschließlich Formulardefinitionen, Ansichten, Regelvorlagen, Antwortvorlagen und so weiter. Dieser alternative Teil wird als Ordner zugeordnete Inhaltstabelle bezeichnet, und der Satz von Nachrichten in der zugeordneten Inhaltstabelle wird als ordner zugeordnete Informationen bezeichnet. Die ausgeblendeten Nachrichten sind integraler Bestandteil des Ordners und werden zusammen mit dem Standardordnerinhalt kopiert, wenn der Ordner kopiert wird. Obwohl physisch als Nachrichten gespeichert, verhalten sich Informationen in der zugeordneten Inhaltstabelle eines Ordners eher wie Eigenschaften als wie angezeigte Nachrichten. Jedes Ordnerobjekt, das eine zugeordnete Inhaltstabelle unterstützt, kann benutzerdefinierte Formulare speichern. Die [IMAPIContainer::GetContentsTable-Methode](imapicontainer-getcontentstable.md) kann abhängig vom Wert des  _Parameters ulflags_ der Methode entweder den Standardinhalt oder den zugeordneten Inhalt des Ordners zurückgeben. 
  
Eine Formularbibliothek besteht aus Formulardefinitionen, die in der zugeordneten Inhaltstabelle eines Ordners gespeichert sind. Die Formulardefinition umfasst die Eigenschaften des Formulars, die aktionen, die das Formular unterstützt, und sogar die ausführbare Datei des Formularservers, die als eine oder mehrere Nachrichtenanlagen gespeichert wird.
  
Darüber hinaus können Formulare in einer beliebigen Datei oder an einem beliebigen Speicherort gespeichert werden, die vom verwendeten Formular-Manager unterstützt wird. Der Standardformular-Manager speichert Formularserver in MAPI-Ordnern, aber ein benutzerdefinierter Formular-Manager könnte einen eigenen Speicher für Formularserver implementieren.
  
Ein Formular kann über mehrere Benutzeroberflächen verfügen, die an seine Nachrichtenklasse gebunden sind. Ein Formular kann z. B. über separate Benutzeroberflächen zum Verfassen und Lesen verfügen. Das Formular übernimmt das Aufrufen der richtigen Benutzeroberfläche für unterschiedliche Benutzeranforderungen, je nachdem, welches der Verben des Formulars aufgerufen wird. Wenn ihr Formularserver beispielsweise über separate Benutzeroberflächen zum Verfassen und Lesen verfügt, kann die Benutzeroberfläche Zum Verfassen automatisch geöffnet werden, wenn der Benutzer eine neue Nachricht der Nachrichtenklasse des Formulars erstellt, und die Benutzeroberfläche Lesen kann automatisch geöffnet werden, wenn der Benutzer eine vorhandene Nachricht der Nachrichtenklasse des Formulars öffnet.
  
Die meisten in einer Formulardefinition gespeicherten Informationen sind durch Aufrufen der [IMAPIFormInfo::IMAPIProp-Methode](imapiforminfoimapiprop.md) für ein **IMAPIFormInfo-Objekt** verfügbar. Die **IMAPIFormInfo-Schnittstelle** vereinfacht den Zugriff auf Formularinformationen, indem alle zum Abrufen der Informationen erforderlichen MAPI-Ordner- und Nachrichtenmethoden aufgerufen werden. Ein **IMAPIFormInfo-Objekt** kann durch Aufrufen der [IMAPIFormContainer::ResolveMessageClass-Methode erhalten](imapiformcontainer-resolvemessageclass.md) werden. 
  
Die drei Arten von Formularbibliotheken werden in den Themen [Lokale Formularbibliotheken,](local-form-libraries.md) [Ordnerformularbibliotheken](folder-form-libraries.md) und [Persönliche Formularbibliotheken beschrieben.](personal-form-libraries.md)
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Formulare](mapi-forms.md)

