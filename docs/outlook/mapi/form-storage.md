---
title: Formular Speicher
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6ddf9158-3c10-408a-aeaf-5a382c4339e7
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a99ef76e63e634c661bf82bdab10b86c843e0df0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791726"
---
# <a name="form-storage"></a>Formular Speicher

**Betrifft**: Outlook 
  
Obwohl es nicht erforderlich ist, wissen Sie alle Details der wie Formulare physisch gespeichert sind, ist es sinnvoll, nur einige der wichtigsten Konzepte verstehen. Bevor Sie die drei Typen von Formularbibliotheken mithilfe der Standard-Formular-Manager unterstützt beschreiben, bietet in diesem Thema daher eine Übersicht über wie Formulare gespeichert werden.
  
Formulardefinitionen können in Ordnern in eine oder mehrere MAPI-Nachrichtenspeicher physisch gespeichert werden. Jedes MAPI-Ordners mit zwei Bereichen zum Speichern von Message-Objekten betrachtet werden kann: das standard-Webpart und das zugeordnete Teil. Der standard Teil des Ordners enthält die Nachrichten und Ordnern, die Benutzer zu bearbeiten.
  
Das zugeordnete Teil umfasst ausgeblendete Nachricht-Objekte, die dem Ordner, einschließlich Formulardefinitionen, Ansichten, Vorlagen, Antwortvorlagen usw. zugeordnet sind. Diese Alternative Teil die Ordner verknüpfte Inhaltstabelle wird aufgerufen, und der Satz von Nachrichten in der zugehörigen Inhaltstabelle genannt wird die Informationen Ordner verknüpft ist. Die ausgeblendeten Nachrichten sind ein integraler Bestandteil des Ordners und werden zusammen mit den Standardordner Inhalt kopiert, wenn der Ordner kopiert wird. Obwohl physisch als Nachrichten gespeichert, unterscheidet sich Informationen in einem Ordner zugeordnete Inhaltstabelle mehr Eigenschaften als sichtbare Nachrichten wie. Alle Folder-Objekt, das eine Inhaltstabelle zugeordneten unterstützt kann zum Speichern von benutzerdefinierten Formularen. Die [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) -Methode kann den Inhalt standard oder den zugehörigen Inhalt des Ordners, abhängig vom Wert des Parameters für die Methode _Ulflags_ zurückgeben. 
  
Besteht aus eine Formularbibliothek Formulardefinitionen, die in einem Ordner zugeordnete Inhaltstabelle gespeichert. Die Formulardefinition enthält die Eigenschaften des Formulars, die Aktionen des Formulars unterstützt, und auch das Formular Server ausführbare Datei, die als eine oder mehrere e-Mail-Anlagen gespeichert ist.
  
Darüber hinaus können Formulare in eine Datei oder einen Speicherort, der der Formular-Manager verwendeten unterstützt gespeichert werden. Der Standard-Formular-Manager speichert Formular Servern in MAPI-Ordnern, aber ein benutzerdefiniertes Formular-Manager konnte einen eigene Speicher für Formular-Servern implementieren.
  
Ein Formular kann mehrere Benutzeroberflächen enthalten, die auf deren Nachrichtenklasse gebunden sind. Beispielsweise kann ein Formular separate verfassen- und Benutzeroberflächen haben. Das Formular akzeptiert Pflege des Aufrufs der entsprechenden Benutzeroberfläche für verschiedene Benutzeranfragen, je nachdem, welches das Formular Verben angerufen wird. Angenommen, wenn Ihr Formular Server separaten Verfassen und Lesen von Benutzeroberflächen verfügt, die Benutzeroberfläche zum Verfassen kann geöffnet werden automatisch, wenn der Benutzer eine neue Nachricht der Nachrichtenklasse des Formulars erstellt und die Read-Benutzeroberfläche geöffnet werden automatisch bei der Benutzer öffnet eine vorhandene Nachricht der Nachrichtenklasse des Formulars.
  
Die meisten der Informationen in einer Formulardefinition ist durch Aufrufen der [IMAPIFormInfo::IMAPIProp](imapiforminfoimapiprop.md) -Methode für ein Objekt **IMAPIFormInfo** verfügbar. Die Schnittstelle **IMAPIFormInfo** vereinfacht den Zugriff auf Informationen für das Formular durch Aufrufen der MAPI-Ordner und die Nachricht angewendet werden, um die Informationen abzurufen. Ein **IMAPIFormInfo** -Objekt kann durch Aufrufen der Methode [IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) abgerufen werden. 
  
Die drei Typen von Formularbibliotheken werden in den Themen [Lokalen Formularbibliotheken](local-form-libraries.md), [Ordner Formularbibliotheken](folder-form-libraries.md) und [Persönliche Formularbibliotheken](personal-form-libraries.md)beschrieben.
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Formulare](mapi-forms.md)

