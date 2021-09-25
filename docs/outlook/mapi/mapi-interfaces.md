---
title: MAPI-Schnittstellen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 34a66cf0-b4e0-4fd5-b937-cd157888961d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1b8d0fb625270422eb1910154afcada906b8dccd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610286"
---
# <a name="mapi-interfaces"></a>MAPI-Schnittstellen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Dokumentation für jede Schnittstelle besteht aus einem einleitenden Abschnitt, der eine kurze Beschreibung des Zwecks der Schnittstelle enthält, , gefolgt von einer Tabelle, die die folgenden Informationen enthält.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Die Headerdatei, in der die Schnittstelle definiert ist, und die beim Kompilieren des Quellcodes einbezogen werden muss.  <br/> |
|Verf�gbar gemacht von:  <br/> |Das Objekt, das die Schnittstelle verf�gbar macht.  <br/> |
|Implementiert von:  <br/> |Eine Liste der Komponenten, die eine Implementierung der Schnittstelle bereitstellen.  <br/> |
|Aufgerufen von:  <br/> |Eine Liste der Komponenten, die in der Regel die Methoden der Schnittstelle aufrufen.  <br/> |
|Schnittstellenbezeichner:  <br/> |Die GUID des Schnittstellenbezeichners.  <br/> |
|Zeigertyp:  <br/> |Der Zeigertyp f�r das Objekt, das die Schnittstelle verf�gbar macht.  <br/> |
|Transaktionsmodell:  <br/> |F�r von [IMAPIProp](imapipropiunknown.md) abgeleitete Schnittstellen. Bei �nontransacted" werden die �nderungen sofort wirksam; bei �transacted" werden die �nderungen erst wirksam, wenn [IMAPIProp::SaveChanges](imapiprop-savechanges.md) aufgerufen wird.  <br/> |
   
Nach der ersten Tabelle folgt eine weitere Tabelle, in der alle Methoden dieser Schnittstelle in der vtable-Reihenfolge aufgelistet sind. Bei einer vtable handelt es sich um ein Array von Funktionszeigern, die von dem Compiler mit einem Funktionszeiger f�r jede Methode eines MAPI-Objekts erstellt werden. Die Methoden werden in der gleichen Reihenfolge aufgelistet, in der sie deklariert sind. Methoden, die von anderen Schnittstellen geerbt werden, sind nicht in der Tabelle in vtable-Reihenfolge dargestellt, k�nnen jedoch auf die gleiche Art und Weise verwendet werden, wie in der Schnittstelle dokumentiert, die sie definiert.
  
Nach jedem Schnittstellenthema werden dann die Methoden der Schnittstelle in alphabetischer Reihenfolge dokumentiert. Die Dokumentation umfasst f�r jede Methode umfasst eine kurze Beschreibung des Zwecks, einen Syntaxblock sowie die folgenden Informationen.
  
|**�berschrift**|**Inhalt**|
|:-----|:-----|
|Parameter  <br/> |Eine Beschreibung der einzelnen Parameter in der Methode.  <br/> |
|Rückgabewert  <br/> |Eine Beschreibung der eindeutigen Werte, die die Methode zur�ckgeben kann. Dies sind die Werte, nach denen Anrufer in ihrem Code suchen sollten.  <br/> |
|Bemerkungen  <br/> |Eine Beschreibung davon, warum und wie die Methode verwendet wird.  <br/> |
|Siehe auch  <br/> |Querverweise zu anderen Themen in dieser Referenz.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI Reference](mapi-reference.md)

