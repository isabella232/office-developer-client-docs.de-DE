---
title: Übersicht über Typ von MAPI-Eigenschaft
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b762f5fb-7c2c-4303-96f7-0b6e657146c9
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ce3cd37247f37c4e70adb07769f00b2df07307a3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793051"
---
# <a name="mapi-property-type-overview"></a>Übersicht über Typ von MAPI-Eigenschaft
  
**Betrifft**: Outlook 
  
Eigenschaftentypen sind Konstanten, die von MAPI in der MAPIDEFS definiert. H-Headerdatei, die den zugrunde liegenden Daten eines Eigenschaftswerts anzugeben. Alle Eigenschaften verwenden, ob sie, MAPI, Clientanwendungen oder Dienstanbieter definiert sind, Sie eine der folgenden Typen. 
  
Eigenschaftentypen Namenskonvention ähnliche für Eigenschaftentags verwendeten ähnelt. Viele Eigenschaftentypen haben eine Single-Wert und mehreren Werten Version. Eigenschaften der einzelnen Werte enthalten ein Wert des Typs wie eine einzelne ganze Zahl oder eine Zeichenfolge. Die Konstante, die zur Darstellung einer einzelnen Value-Eigenschaft besteht aus zwei Teilen: Präfix PT_ und eine Zeichenfolge, die den tatsächlichen Typ, wie lange oder des STRING8 beschreibt. 
  
Eigenschaften mit mehreren Werten enthalten mehrere Werte des Typs. Im Gegensatz zu OLE-variant-Arrays ist jeden Wert in einer mehrwertigen Eigenschaft des gleichen Typs. Die Konstante, die zur Darstellung von mehrwertiger Eigenschaften wird erstellt, durch die Kombination der MV_FLAG Flag mit der entsprechenden Einzelwert-Konstante, die den Basistyp darstellt. Es gibt drei Teile: das Präfix PT_ gefolgt von MV_ gefolgt von einer Zeichenfolge, die den Typ beschreibt. Beispielsweise der Typ für eine Eigenschaft mit mehreren ganzen Zahlen ist PT_MV_LONG und für mehrere Zeichenfolgen PT_MV_STRING8.
  
Die folgende Abbildung zeigt die Struktur einer [SPropValue](spropvalue.md) -Struktur, um eine mehrwertige ganze Zahl, eine Eigenschaft vom Typ PT_MV_LONG zu beschreiben. **Das Element** wird erweitert, um die Anzahl der Werte für ganze Zahl in die Eigenschaft sowie einen Zeiger auf ein Array der folgenden Werte enthalten. 
  
**Eigenschaften mit mehreren Werten**
  
![Eigenschaften mit mehreren Werten] (media/amapi_12.gif "Eigenschaften mit mehreren Werten")
  
Obwohl die Unterstützung für mehrwertige Eigenschaften ist optional, empfiehlt MAPI-Clients und -Dienstanbieter unterstützen beide Arten von Eigenschaften, da in diesem Fall ermöglicht mehr Interaktion zwischen MAPI-kompatible Komponenten wie folgt.
  
Die folgende Abbildung zeigt eine Liste aller der verschiedenen Konstanten des Eigenschaftentyps, anzeigen, wo sie in einer Struktur **SPropValue** gespeichert sind. Die Größe des Elements **Wert** ist abhängig von den angegebenen Typ. Beachten Sie, dass nicht alle Typen einwertig mehrwertige-Entsprechungen. 
  
**Eigenschaftstypenkonstanten**
  
![Konstanten des Eigenschaftentyps] (media/amapi_11.gif "Konstanten des Eigenschaftentyps")
  
Clients und Arbeiten mit einer Eigenschaft Dienstanbieter müssen zwei Schritte ausführen:
  
1. Bestimmen Sie, ob die Eigenschaft verfügbar oder nicht verfügbar ist.
    
2. Falls verfügbar, rufen Sie den Wert der Eigenschaft ab.
    
In einigen Fällen muss einen Client oder Dienstanbieter nur das Vorhandensein einer Eigenschaft überprüfen. in anderen Fällen ist es erforderlich, nach einem bestimmten Wert zu überprüfen. Beispielsweise Transportanbieter haben drei verschiedene Kurse der Aktion für die Verarbeitung der **PR\_SEND_RICH_INFO** -Eigenschaft ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), einen booleschen Wert, der angibt, ob eine Nachricht mit gesendet werden sollen formatierter Text. Wenn **PR\_SEND_RICH_INFO** ist auf TRUE festgelegt wird, überträgt der Adressbuchhierarchie formatierten Text. Wenn sie auf "false" festgelegt ist, wird der formatierte Text vor der Übertragung verworfen. Wenn **PR_SEND_RICH_INFO** nicht verfügbar ist, folgt der Adressbuchhierarchie seiner standardmäßigen Vorgehensweise aufbauen, d. h. für den bestimmten Anbieter. 
  
MAPI definiert einen speziellen Eigenschaftentyp PT_UNSPECIFIED, die ein Client oder Dienstanbieter verwenden können, um eine Eigenschaft abzurufen, wenn der Eigenschaftentyp nicht bekannt ist. Zum Abrufen einer Eigenschaft ohne Vorauswissen des Typs ein Client oder Dienstanbieter ein Objekt [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode aufgerufen und übergibt ein Bezeichner für die Eigenschaft und den Eigenschaftentyp PT_UNSPECIFIED bestehen Eigenschaftentag. **GetProps** gibt eine [SPropValue](spropvalue.md) -Struktur für die Eigenschaft PT_UNSPECIFIED mit den entsprechenden Typ ersetzen. Implementieren von **GetProps** Dienstanbieter sind zur Unterstützung von PT_UNSPECIFIED erforderlich. 
  
Einige MAPI-Objekte unterstützen Eigenschaften, die sich selbst sind Objekte. Objekteigenschaften haben die PT_OBJECT. Statt **IMAPIProp::GetProps** diese Eigenschaften, Clients und -Dienstanbieter in der Regel Zugriff auf Benutzer entweder die [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode, die entsprechende Schnittstelle für den Zugriff oder eine Methode für das Objekt angeben die Eigenschaft unterstützt. 
  
Da zugreifen auf den Wert einer Objekteigenschaft beinhaltet die Verwendung einer der Schnittstellen für das Objekt **GetProps** ist nicht zulässig. Mit **GetProps**greift der Aufrufer den Wert einer Eigenschaft über eine **SPropValue** -Struktur auf. Mit **IMAPIProp::OpenProperty**ruft der Aufrufer einen Zeiger auf eine Schnittstelle, die das Objekt zugreifen kann. **OpenProperty** können immer verwendet werden, um eine Object-Eigenschaft abzurufen. Eine weitere Möglichkeit, Aufrufen einer Methode für das Objekt ist nicht mit jeder Eigenschaft-Objekts verfügbar. 
  
Jeder Ordner unterstützt beispielsweise zwei Tabellen, eine Hierarchietabelle und Inhalt. Diese Tabellen sind die Eigenschaften des Ordners. Ihre Eigenschaftentags sind **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) und **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)). Tabellen sind Objekte, die die **IMAPITable** -Schnittstelle für den Zugriff benötigen. Ein Client kann den Ordner [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) -Methode zum Zugriff auf die Hierarchietabelle, den Ordner [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) -Methode den Zugriff auf die Inhaltstabelle oder des Ordners [IMAPIProp::OpenProperty aufrufen. ](imapiprop-openproperty.md)-Methode, um die beiden Tabellen zugreifen. Zum Aufrufen von **OpenProperty**übergibt ein Client das Eigenschafts-Tag für die Eigenschaft als der erste Parameter und als Schnittstellenbezeichner für die Schnittstelle für den Zugriff als der zweite Parameter verwendet werden soll. Diese Parameter wäre **PR_CONTAINER_HIERARCHY** oder **PR_CONTAINER_CONTENTS** und **IID_IMAPITable**.
  
Eine vollständige Liste der Eigenschaftentypen einwertig und mehrwertige finden Sie unter [Eigenschaftentypen](property-types.md). 
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über die MAPI-Eigenschaft](mapi-property-overview.md)

