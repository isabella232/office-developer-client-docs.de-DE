---
title: Formularspeicher
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 6ddf9158-3c10-408a-aeaf-5a382c4339e7
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e41876c3a5f1a36285a2ab766108fa8f7129c0af
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59587965"
---
# <a name="form-storage"></a>Formularspeicher

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Obwohl es nicht erforderlich ist, alle Details darüber zu kennen, wie Formulare physisch gespeichert werden, ist es hilfreich, einige der Hauptkonzepte zu verstehen. Daher bietet dieses Thema vor der Beschreibung der drei typen von Formularbibliotheken, die vom Standardformular-Manager unterstützt werden, eine Übersicht über die Speicherung von Formularen.
  
Formulardefinitionen können physisch in Ordnern in einem oder mehreren MAPI-Nachrichtenspeichern gespeichert werden. Jeder MAPI-Ordner kann als zwei Bereiche zum Speichern von Nachrichtenobjekten betrachtet werden: der Standardteil und der zugeordnete Teil. Der Standardteil des Ordners enthält die Nachrichten und Ordner, die Benutzer bearbeiten.
  
Der zugeordnete Teil enthält ausgeblendete Nachrichtenobjekte, die dem Ordner zugeordnet sind, einschließlich Formulardefinitionen, Ansichten, Regelvorlagen, Antwortvorlagen usw. Dieser alternative Teil wird als Ordnerinhaltsverzeichnis bezeichnet, und der Nachrichtensatz im zugeordneten Inhaltsverzeichnis wird als ordnerbezogene Informationen bezeichnet. Die ausgeblendeten Nachrichten sind ein integraler Bestandteil des Ordners und werden zusammen mit dem Standardordnerinhalt kopiert, wenn der Ordner kopiert wird. Obwohl Informationen in der zugeordneten Inhaltstabelle eines Ordners physisch als Nachrichten gespeichert werden, verhalten sie sich eher wie Eigenschaften als wie sichtbaren Nachrichten. Jedes Ordnerobjekt, das ein zugeordnetes Inhaltsverzeichnis unterstützt, kann benutzerdefinierte Formulare speichern. Die [IMAPIContainer::GetContentsTable-Methode](imapicontainer-getcontentstable.md) kann abhängig vom Wert des  _Parameters " enumerations"_ der Methode entweder den Standardinhalt oder den zugeordneten Inhalt des Ordners zurückgeben. 
  
Eine Formularbibliothek besteht aus Formulardefinitionen, die in der zugeordneten Inhaltstabelle eines Ordners gespeichert sind. Die Formulardefinition enthält die Eigenschaften des Formulars, die aktionen, die das Formular unterstützt, und sogar die ausführbare Datei des Formularservers, die als eine oder mehrere Nachrichtenanlagen gespeichert ist.
  
Darüber hinaus können Formulare in jeder Datei oder an jedem Speicherort gespeichert werden, die der verwendete Formular-Manager unterstützt. Der Standardformular-Manager speichert Formularserver in MAPI-Ordnern, aber ein benutzerdefinierter Formular-Manager könnte einen eigenen Speicher für Formularserver implementieren.
  
Ein Formular kann mehrere Benutzeroberflächen aufweisen, die an seine Nachrichtenklasse gebunden sind. Beispielsweise kann ein Formular über separate Benutzeroberflächen zum Verfassen und Lesen verfügen. Das Formular übernimmt das Aufrufen der richtigen Benutzeroberfläche für verschiedene Benutzeranforderungen, je nachdem, welche verben des Formulars aufgerufen wird. Wenn der Formularserver beispielsweise über separate Benutzeroberflächen zum Verfassen und Lesen verfügt, kann die Benutzeroberfläche zum Verfassen automatisch geöffnet werden, wenn der Benutzer eine neue Nachricht der Nachrichtenklasse des Formulars erstellt, und die Benutzeroberfläche "Lesen" kann automatisch geöffnet werden, wenn der Benutzer eine vorhandene Nachricht der Nachrichtenklasse des Formulars öffnet.
  
Die meisten in einer Formulardefinition gespeicherten Informationen sind durch Aufrufen der [IMAPIFormInfo::IMAPIProp-Methode](imapiforminfoimapiprop.md) für ein **IMAPIFormInfo-Objekt** verfügbar. Die **IMAPIFormInfo-Schnittstelle** vereinfacht den Zugriff auf Formularinformationen, indem alle MAPI-Ordner und Nachrichtenmethoden aufgerufen werden, die zum Abrufen der Informationen erforderlich sind. Ein **IMAPIFormInfo** -Objekt kann durch Aufrufen der [IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) -Methode abgerufen werden. 
  
Die drei Typen von Formularbibliotheken werden in den Themen ["Lokale Formularbibliotheken",](local-form-libraries.md) ["Ordnerformularbibliotheken"](folder-form-libraries.md) und ["Persönliche Formularbibliotheken"](personal-form-libraries.md)beschrieben.
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Formulare](mapi-forms.md)

