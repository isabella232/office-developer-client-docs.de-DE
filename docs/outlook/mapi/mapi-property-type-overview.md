---
title: Übersicht über die MAPI-Eigenschaftstypen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b762f5fb-7c2c-4303-96f7-0b6e657146c9
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 58dd25f09b76d97fd6441915225756a19f4ec3cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328260"
---
# <a name="mapi-property-type-overview"></a>Übersicht über die MAPI-Eigenschaftstypen
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eigenschaftstypen sind Konstanten, die von MAPI in der MAPIDEFS definiert werden. H-Headerdatei, die den zugrunde liegenden Datentyp eines Eigenschaftswerts angibt. Alle Eigenschaften, unabhängig davon, ob Sie von MAPI, von Clientanwendungen oder von Dienstanbietern definiert werden, verwenden einen dieser Typen. 
  
Eigenschaftstypen Folgen einer ähnlichen Benennungskonvention wie die für Eigenschaftstags. Viele Eigenschaftstypen verfügen über eine Einzel-und eine mehrwertige Version. Einzelne Werte Eigenschaften enthalten einen Wert des Typs, beispielsweise eine einzelne ganze Zahl oder Zeichenfolge. Die zur Darstellung einer einzelnen Value-Eigenschaft verwendete Konstante besteht aus zwei Teilen: dem Präfix PT_ und einer Zeichenfolge, die den tatsächlichen Typ beschreibt, beispielsweise LONG oder STRING8. 
  
Mehrwertige Eigenschaften enthalten mehr als einen Wert des Typs. Im Gegensatz zu OLE-Variant-Arrays hat jeder Wert in einer mehrwertigen Eigenschaft denselben Typ. Die zur Darstellung von mehrwertigen Eigenschaften verwendete Konstante wird erstellt, indem das MV_FLAG-Flag mit der entsprechenden Einzel wertkonstante kombiniert wird, die den Basistyp darstellt. Es gibt drei Teile: das Präfix PT_ gefolgt von MV_ gefolgt von einer Zeichenfolge, die den Typ beschreibt. Beispielsweise ist der Typ für eine Eigenschaft, die mehrere ganze Zahlen enthält, PT_MV_LONG und für mehrere Zeichenfolgen PT_MV_STRING8.
  
Die folgende Abbildung zeigt die Struktur einer [SPropValue](spropvalue.md) -Struktur zur Beschreibung einer mehrwertigen Ganzzahl, einer Eigenschaft vom Typ PT_MV_LONG. Der **Wert** Member wird erweitert, um die Anzahl der ganzzahligen Werte in der Eigenschaft und einen Zeiger auf ein Array dieser Werte einzuschließen. 
  
**Eigenschaften mit mehreren Werten**
  
![Mehr] wertige Eigenschaften (media/amapi_12.gif "Mehr") wertige Eigenschaften
  
Obwohl die Unterstützung für Eigenschaften mit mehreren Werten optional ist, empfiehlt MAPI, dass Clients und Dienstanbieter beide Arten von Eigenschaften unterstützen, da dadurch eine bessere Interaktion zwischen MAPI-kompatiblen Komponenten ermöglicht wird.
  
In der folgenden Abbildung sind alle verschiedenen Eigenschaftentyp Konstanten aufgeführt, die zeigen, wo Sie in einer **SPropValue** -Struktur gespeichert sind. Die Größe des **value** -Elements hängt vom jeweiligen Typ ab. Beachten Sie, dass nicht alle einwertigen Typen mehrwertige äquivalente aufweisen. 
  
**Eigenschaftstypenkonstanten**
  
![Eigenschaftentyp Konstanten] (media/amapi_11.gif "Eigenschaftentyp Konstanten")
  
Clients und Dienstanbieter, die mit einer Eigenschaft arbeiten, müssen zwei Schritte ausführen:
  
1. Bestimmen Sie, ob die Eigenschaft verfügbar oder nicht verfügbar ist.
    
2. Wenn verfügbar, rufen Sie den Wert der Eigenschaft ab.
    
Manchmal muss ein Client oder Dienstanbieter nur überprüfen, ob eine Eigenschaft vorhanden ist; Manchmal ist es erforderlich, einen bestimmten Wert zu überprüfen. Transportanbieter haben beispielsweise drei verschiedene Vorgehensweisen für die Verarbeitung **der\_PR-SEND_RICH_INFO** ([pidtagsendrichinfo (](pidtagsendrichinfo-canonical-property.md))-Eigenschaft, einen booleschen Wert, der angibt, ob eine Nachricht mit formatierter Text. Wenn **PR\_SEND_RICH_INFO** auf true festgelegt ist, übermittelt der Transportanbieter den formatierten Text. Wenn Sie auf FALSE festgelegt ist, wird der formatierte Text vor der Übertragung verworfen. Wenn **PR_SEND_RICH_INFO** nicht verfügbar ist, folgt der Transportanbieter seiner standardmäßigen Vorgehensweise, was auch immer für den jeweiligen Anbieter gilt. 
  
MAPI definiert einen speziellen Eigenschaftentyp, PT_UNSPECIFIED, der von einem Client oder Dienstanbieter zum Abrufen einer Eigenschaft verwendet werden kann, wenn der Eigenschaftentyp unbekannt ist. Um eine Eigenschaft ohne Vorkenntnisse des Typs abzurufen, Ruft ein Client oder Dienstanbieter die [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode eines Objekts auf und übergibt ein Eigenschaftentag, das aus dem Bezeichner der Eigenschaft und dem PT_UNSPECIFIED-Eigenschaftentyp besteht. **** GetProps gibt eine [SPropValue](spropvalue.md) -Struktur für die Eigenschaft zurück, die PT_UNSPECIFIED durch den entsprechenden Typ ersetzt. Dienstanbieter, **** die GetProps implementieren, sind zur Unterstützung von PT_UNSPECIFIED erforderlich. 
  
Einige MAPI-Objekte unterstützen Eigenschaften, die selbst Objekte sind. Objekteigenschaften haben den Typ PT_OBJECT. Statt **IMAPIProp::** GetProps für den Zugriff auf diese Eigenschaften zu verwenden, werden Clients und Dienstanbieter in der Regel entweder die [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode, die die entsprechende Schnittstelle für Access oder eine Methode für das Objekt angibt. unterstützen der Eigenschaft. 
  
Da der Zugriff auf den Wert einer Objekteigenschaft die Verwendung einer der Schnittstellen für das Objekt **** beinhaltet, ist GetProps unangemessen. Mit **** GetProps greift der Aufrufer über eine **SPropValue** -Struktur auf den Wert einer Eigenschaft zu. Mit **IMAPIProp:: OpenProperty**ruft der Aufrufer einen Zeiger auf eine Schnittstelle ab, die auf das Objekt zugreifen kann. **OpenProperty** kann immer verwendet werden, um eine Objekteigenschaft abzurufen. Die andere Option, die eine Methode für das Objekt aufruft, ist bei jeder Objekteigenschaft nicht verfügbar. 
  
Jeder Ordner unterstützt beispielsweise zwei Tabellen, eine Hierarchietabelle und eine Inhaltstabelle. Diese Tabellen sind Eigenschaften des Ordners; Ihre Eigenschaftstags sind **PR_CONTAINER_HIERARCHY** ([Pidtagcontainerhierarchy (](pidtagcontainerhierarchy-canonical-property.md)) und **PR_CONTAINER_CONTENTS** ([pidtagcontainercontents (](pidtagcontainercontents-canonical-property.md)). Tabellen sind Objekte, die die **IMAPITable** -Schnittstelle für den Zugriff erfordern. Ein Client kann die [IMAPIContainer:: GetHierarchy](imapicontainer-gethierarchytable.md) -Methode des Ordners aufrufen, um auf die Hierarchietabelle zuzugreifen, die [IMAPIContainer::](imapicontainer-getcontentstable.md) getcontentable-Methode des Ordners für den Zugriff auf die Inhaltstabelle oder die [IMAPIProp:: OpenProperty des Ordners. ](imapiprop-openproperty.md)Methode für den Zugriff auf eine Tabelle. Um **OpenProperty**aufzurufen, übergibt ein Client das Property-Tag für die Eigenschaft als ersten Parameter und einen Schnittstellenbezeichner für die Schnittstelle, die für Access als zweiten Parameter verwendet werden soll. Diese Parameter sind **PR_CONTAINER_HIERARCHY** oder **PR_CONTAINER_CONTENTS** und **IID_IMAPITable**.
  
Eine vollständige Liste der Eigenschaftentypen mit einem oder mehreren Werten finden Sie unter [Property Types](property-types.md). 
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über die MAPI-Eigenschaft](mapi-property-overview.md)

