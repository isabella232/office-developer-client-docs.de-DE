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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328084"
---
# <a name="form-storage"></a>Formularspeicher

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Obwohl es nicht notwendig ist, alle Details der physischen Speicherung von Formularen zu kennen, ist es hilfreich, einige der wichtigsten Konzepte zu verstehen. Vor Beschreibung der drei Arten von Formularbibliotheken, die vom Standardformular-Manager unterstützt werden, finden Sie in diesem Thema eine Übersicht über die Speicherung von Formularen.
  
Formulardefinitionen können physisch in Ordnern in einem oder mehreren MAPI-Nachrichten speichern gespeichert werden. Jeder MAPI-Ordner kann als zwei Bereiche zum Speichern von Nachrichtenobjekten betrachtet werden: der Standardteil und der zugehörige Teil. Der Standardteil des Ordners enthält die Nachrichten und Ordner, die von Benutzern bearbeitet werden.
  
Der zugeordnete Teil enthält ausgeblendete Nachrichtenobjekte, die dem Ordner zugeordnet sind, einschließlich Formulardefinitionen, Ansichten, Regelvorlagen, Antwortvorlagen usw. Dieser Alternative Teil wird als Folder-Associated Contents-Tabelle bezeichnet, und die Gruppe der Nachrichten in der zugeordneten Inhaltstabelle wird als Ordner zugeordnete Informationen bezeichnet. Die ausgeblendeten Nachrichten sind ein integraler Bestandteil des Ordners und werden zusammen mit den standardmäßigen Ordnerinhalten kopiert, wenn der Ordner kopiert wird. Obwohl physisch als Nachrichten gespeichert, verhält sich die Informationen in der Tabelle mit den zugeordneten Inhalten eines Ordners mehr als Eigenschaften wie sichtbare Nachrichten. Jedes Folder-Objekt, das eine zugeordnete Inhaltstabelle unterstützt, kann benutzerdefinierte Formulare speichern. Die [IMAPIContainer::](imapicontainer-getcontentstable.md) getcontentable-Methode kann je nach Wert des _ulflags_ -Parameters der Methode entweder den Standardinhalt oder den zugeordneten Inhalt des Ordners zurückgeben. 
  
Eine Formularbibliothek besteht aus Formulardefinitionen, die in der Tabelle zugeordnete Inhalte eines Ordners gespeichert sind. Die Formulardefinition enthält die Eigenschaften des Formulars, die Aktionen, die vom Formular unterstützt werden, und sogar die ausführbare Datei des Formular Servers, die als eine oder mehrere Nachrichtenanlagen gespeichert wird.
  
Darüber hinaus können Formulare in jeder beliebigen Datei oder jedem Speicherort gespeichert werden, die der verwendete Formular-Manager unterstützt. Der Standardformular-Manager speichert Formularserver in MAPI-Ordnern, aber ein benutzerdefinierter Formular-Manager kann einen eigenen Speicher für Formularserver implementieren.
  
Ein Formular kann mehrere Benutzeroberflächen aufweisen, die an seine Nachrichtenklasse gebunden sind. Ein Formular kann beispielsweise separate verFassen-und Lese-Benutzeroberflächen aufweisen. Das Formular sorgt dafür, dass die richtige Benutzeroberfläche für unterschiedliche Benutzeranforderungen aufgerufen wird, je nachdem, welche Verben des Formulars aufgerufen werden. Wenn Ihr Formularserver beispielsweise über separate Erstellungs-und Lese-Benutzeroberflächen verfügt, kann die Erstell-Benutzeroberfläche automatisch geöffnet werden, wenn der Benutzer eine neue Nachricht der Nachrichtenklasse des Formulars erstellt, und die Lese-Benutzeroberfläche kann automatisch geöffnet werden, wenn der der Benutzer öffnet eine vorhandene Nachricht der Nachrichtenklasse des Formulars.
  
Die meisten in einer Formulardefinition gespeicherten Informationen stehen zur Verfügung, indem die [IMAPIFormInfo:: IMAPIProp](imapiforminfoimapiprop.md) -Methode für ein **IMAPIFormInfo** -Objekt aufgerufen wird. Die **IMAPIFormInfo** -Schnittstelle vereinfacht den Zugriff auf Formular Informationen durch Aufrufen aller MAPI-Ordner-und Nachrichten Methoden, die zum Abrufen der Informationen erforderlich sind. Ein **IMAPIFormInfo** -Objekt kann abgerufen werden, indem die [IMAPIFormContainer:: ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) -Methode aufgerufen wird. 
  
Die drei Arten von Formularbibliotheken werden in den Themen [lokale Formularbibliotheken](local-form-libraries.md), [Ordner Formularbibliotheken](folder-form-libraries.md) und [persönliche Formularbibliotheken](personal-form-libraries.md)beschrieben.
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Formulare](mapi-forms.md)

