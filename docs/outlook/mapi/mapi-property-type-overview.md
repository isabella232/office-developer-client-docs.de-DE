---
title: Übersicht über den MAPI-Eigenschaftstyp
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: b762f5fb-7c2c-4303-96f7-0b6e657146c9
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 0bdb1c2a631b80015dbc88dbe5a274c0f9b3050b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600806"
---
# <a name="mapi-property-type-overview"></a>Übersicht über den MAPI-Eigenschaftstyp
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eigenschaftstypen sind Konstanten, die von MAPI in MAPIDEFS definiert werden. H-Headerdatei, die den zugrunde liegenden Datentyp eines Eigenschaftswerts angibt. Alle Eigenschaften, unabhängig davon, ob sie durch die MAPI, von Clientanwendungen oder von Dienstanbietern definiert werden, verwenden einen dieser Typen. 
  
Eigenschaftstypen folgen einer ähnlichen Benennungskonvention wie für Eigenschaftstags. Viele Eigenschaftstypen haben sowohl eine Einzelwertversion als auch eine Version mit mehreren Werten. Einwertige Eigenschaften enthalten einen Wert vom Typ, z. B. eine einzelne ganze Zahl oder eine Zeichenfolge. Die Konstante, die zur Darstellung einer Einzelnen-Wert-Eigenschaft verwendet wird, hat zwei Teile: das Präfix PT_ und eine Zeichenfolge, die den tatsächlichen Typ beschreibt, z. B. LONG oder STRING8. 
  
Eigenschaften mit mehreren Werten enthalten mehr als einen Wert ihres Typs. Im Gegensatz zu OLE-Variantenarrays hat jeder Wert in einer mehrwertigen Eigenschaft denselben Typ. Die Konstante, die zur Darstellung mehrwertiger Eigenschaften verwendet wird, wird erstellt, indem das MV_FLAG Flag mit der entsprechenden Einwertkonstante kombiniert wird, die den Basistyp darstellt. Es gibt drei Teile: das Präfix PT_ gefolgt von MV_ gefolgt von einer Zeichenfolge, die den Typ beschreibt. Beispielsweise wird der Typ für eine Eigenschaft, die mehrere ganze Zahlen enthält, PT_MV_LONG und für zeichenfolgen mit mehreren Zeichen PT_MV_STRING8.
  
Die folgende Abbildung zeigt die Struktur einer [SPropValue-Struktur,](spropvalue.md) um eine ganze Zahl mit mehreren Werten zu beschreiben, eine Eigenschaft vom Typ PT_MV_LONG. Das **Value-Element** wird erweitert, um die Anzahl der ganzzahligen Werte in der Eigenschaft und einen Zeiger auf ein Array dieser Werte einzuschließen. 
  
**Eigenschaften mit mehreren Werten**
  
![Eigenschaften mit mehreren Werten](media/amapi_12.gif "Eigenschaften mit mehreren Werten")
  
Obwohl die Unterstützung für Mehrfachwerteigenschaften optional ist, empfiehlt MAPI, dass Clients und Dienstanbieter beide Eigenschaftentypen unterstützen, da dies eine bessere Interaktion zwischen MAPI-kompatiblen Komponenten ermöglicht.
  
In der folgenden Abbildung werden alle konstanten Eigenschaftentypen aufgelistet, die zeigen, wo sie in einer **SPropValue-Struktur** gespeichert sind. Die Größe des **Value-Elements** hängt vom jeweiligen Typ ab. Beachten Sie, dass nicht alle einwertigen Typen gleichbedeutend mit mehreren Werten sind. 
  
**Eigenschaftstypenkonstanten**
  
![Eigenschaftstypenkonstanten](media/amapi_11.gif "Eigenschaftstypenkonstanten")
  
Clients und Dienstanbieter, die mit einer Eigenschaft arbeiten, müssen zwei Schritte ausführen:
  
1. Ermitteln Sie, ob die Eigenschaft verfügbar oder nicht verfügbar ist.
    
2. Wenn verfügbar, rufen Sie den Wert der Eigenschaft ab.
    
Manchmal muss ein Client oder Dienstanbieter nur das Vorhandensein einer Eigenschaft überprüfen. in anderen Fällen ist es erforderlich, nach einem bestimmten Wert zu suchen. Transportanbieter haben beispielsweise drei verschiedene Vorgehensweisen für die Verarbeitung der **\_ PR-SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) -Eigenschaft, einen booleschen Wert, der angibt, ob eine Nachricht mit formatiertem Text übertragen werden soll. Wenn **die \_ PR-SEND_RICH_INFO** auf TRUE festgelegt ist, überträgt der Transportanbieter den formatierten Text. Wenn er auf FALSE festgelegt ist, wird der formatierte Text vor der Übertragung verworfen. Wenn **PR_SEND_RICH_INFO** nicht verfügbar ist, folgt der Transportanbieter seinem Standardverhalten, unabhängig davon, was für den jeweiligen Anbieter gilt. 
  
MAPI definiert einen speziellen Eigenschaftentyp, PT_UNSPECIFIED, den ein Client oder Dienstanbieter verwenden kann, um eine Eigenschaft abzurufen, wenn der Eigenschaftentyp unbekannt ist. Um eine Eigenschaft ohne vorherige Kenntnis ihres Typs abzurufen, ruft ein Client oder Dienstanbieter die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) eines Objekts auf und übergibt ein Eigenschaftstag, das aus dem Bezeichner der Eigenschaft und dem PT_UNSPECIFIED Eigenschaftentyp besteht. **GetProps** gibt eine [SPropValue-Struktur](spropvalue.md) für die Eigenschaft zurück, wobei PT_UNSPECIFIED durch den entsprechenden Typ ersetzt wird. Dienstanbieter, die **GetProps** implementieren, müssen PT_UNSPECIFIED unterstützen. 
  
Einige MAPI-Objekte unterstützen Eigenschaften, die selbst Objekte sind. Objekteigenschaften weisen den Typ PT_OBJECT auf. Anstatt **IMAPIProp::GetProps** für den Zugriff auf diese Eigenschaften zu verwenden, verwenden Clients und Dienstanbieter in der Regel entweder die [IMAPIProp::OpenProperty-Methode,](imapiprop-openproperty.md) die die entsprechende Schnittstelle für den Zugriff angibt, oder eine Methode für das Objekt, das die Eigenschaft unterstützt. 
  
Da für den Zugriff auf den Wert einer Objekteigenschaft eine der Schnittstellen für das Objekt verwendet wird, ist **GetProps** nicht geeignet. Mit **GetProps** greift der Aufrufer über eine **SPropValue-Struktur** auf den Wert einer Eigenschaft zu. Mit **IMAPIProp::OpenProperty** ruft der Aufrufer einen Zeiger auf eine Schnittstelle ab, die auf das Objekt zugreifen kann. **OpenProperty** kann immer zum Abrufen einer Objekteigenschaft verwendet werden. Die andere Option, das Aufrufen einer Methode für das Objekt, ist nicht bei jeder Objekteigenschaft verfügbar. 
  
Beispielsweise unterstützt jeder Ordner zwei Tabellen, eine Hierarchietabelle und ein Inhaltsverzeichnis. Diese Tabellen sind Eigenschaften des Ordners. ihre Eigenschaftstags sind **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) und **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)). Tabellen sind Objekte, die die **IMAPITable-Schnittstelle** für den Zugriff benötigen. Ein Client kann die [IMAPIContainer::GetHierarchyTable-Methode](imapicontainer-gethierarchytable.md) des Ordners aufrufen, um auf die Hierarchietabelle zuzugreifen, die [IMAPIContainer::GetContentsTable-Methode des Ordners,](imapicontainer-getcontentstable.md) um auf die Inhaltstabelle zuzugreifen, oder die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) des Ordners, um auf eine der Tabellen zuzugreifen. Zum Aufrufen von **OpenProperty** übergibt ein Client das Eigenschaftstag für die Eigenschaft als ersten Parameter und einen Schnittstellenbezeichner für die Schnittstelle, die für den Zugriff als zweiten Parameter verwendet werden soll. Diese Parameter sind **PR_CONTAINER_HIERARCHY** oder **PR_CONTAINER_CONTENTS** und **IID_IMAPITable.**
  
Eine vollständige Liste der Eigenschaftstypen mit einem und mehreren Werten finden Sie unter ["Property Types".](property-types.md) 
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über die MAPI-Eigenschaft](mapi-property-overview.md)

