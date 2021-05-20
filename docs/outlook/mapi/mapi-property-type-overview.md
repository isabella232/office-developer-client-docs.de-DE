---
title: Übersicht über den MAPI-Eigenschaftstyp
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b762f5fb-7c2c-4303-96f7-0b6e657146c9
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 58dd25f09b76d97fd6441915225756a19f4ec3cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438197"
---
# <a name="mapi-property-type-overview"></a>Übersicht über den MAPI-Eigenschaftstyp
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eigenschaftstypen sind Konstanten, die von MAPI in MAPIDEFS definiert werden. H-Headerdatei, die den zugrunde liegenden Datentyp eines Eigenschaftswerts angibt. Alle Eigenschaften, unabhängig davon, ob sie von MAPI, von Clientanwendungen oder von Dienstanbietern definiert werden, verwenden einen dieser Typen. 
  
Eigenschaftstypen folgen einer ähnlichen Benennungskonvention wie die, die für Eigenschaftstags verwendet wird. Viele Eigenschaftstypen haben sowohl eine Ein-Wert- als auch eine Mehrwertversion. Single valued properties contain one value of its type such as a single integer or character string. Die Konstante, die zum Darstellen einer einzelnen Werteigenschaft verwendet wird, hat zwei Teile: das Präfix PT_ und eine Zeichenfolge, die den tatsächlichen Typ beschreibt, z. B. LONG oder STRING8. 
  
Eigenschaften mit mehreren Wert enthalten mehr als einen Wert des Typs. Im Gegensatz zu OLE-Variantenarrays hat jeder Wert in einer mehrwertigen Eigenschaft denselben Typ. Die konstante, die zum Darstellen mehrwertigen Eigenschaften verwendet wird, wird erstellt, indem das flag MV_FLAG mit der entsprechenden einzelnen Wertkonstante kombiniert wird, die den Basistyp darstellt. Es gibt drei Teile: das Präfix PT_ gefolgt von MV_ gefolgt von einer Zeichenfolge, die den Typ beschreibt. Beispielsweise ist der Typ für eine Eigenschaft mit mehreren ganzen Zahlen PT_MV_LONG und für Zeichenfolgen mit mehreren Zeichen PT_MV_STRING8.
  
Die folgende Abbildung zeigt die Struktur einer [SPropValue-Struktur,](spropvalue.md) um eine ganze Zahl mit mehreren Wert zu beschreiben, eine Eigenschaft vom Typ PT_MV_LONG. Das **Value-Element** wird erweitert, um eine Anzahl der ganzzahligen Werte in der Eigenschaft und einen Zeiger auf ein Array dieser Werte zu enthalten. 
  
**Eigenschaften mit mehreren Werten**
  
![Eigenschaften mit mehreren](media/amapi_12.gif "Wert Mehrere Werte")
  
Obwohl die Unterstützung mehrerer Werteigenschaften optional ist, empfiehlt MAPI, dass Clients und Dienstanbieter beide Eigenschaftentypen unterstützen, da dadurch eine größere Interaktion zwischen MAPI-kompatiblen Komponenten ermöglicht wird.
  
In der folgenden Abbildung sind alle verschiedenen Eigenschaftentypkonstante aufgeführt, die anzeigen, wo sie in einer **SPropValue-Struktur gespeichert** sind. Die Größe des **Value-Mitglieds** hängt vom jeweiligen Typ ab. Beachten Sie, dass nicht alle Ein-Wert-Typen über Äquivalente mit mehreren Wert verfügen. 
  
**Eigenschaftstypenkonstanten**
  
![Eigenschaftentypkonstante](media/amapi_11.gif "Eigenschaftentypkonstante")
  
Clients und Dienstanbieter, die mit einer Eigenschaft arbeiten, müssen zwei Schritte ausführen:
  
1. Ermitteln Sie, ob die Eigenschaft verfügbar oder nicht verfügbar ist.
    
2. Wenn verfügbar, rufen Sie den Wert der Eigenschaft ab.
    
Manchmal muss ein Client oder Dienstanbieter nur auf das Vorhandensein einer Eigenschaft überprüfen. in anderen Zeiten ist es erforderlich, nach einem bestimmten Wert zu suchen. Beispielsweise verfügen Transportanbieter über drei verschiedene Aktionswege für die Verarbeitung der **PR \_ SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) -Eigenschaft, ein boolescher Wert, der angibt, ob eine Nachricht mit formatierten Text übertragen werden soll. Wenn **pr \_ SEND_RICH_INFO** auf TRUE festgelegt ist, überträgt der Transportanbieter den formatierten Text. Wenn er auf FALSE festgelegt ist, wird der formatierte Text vor der Übertragung verworfen. Wenn **PR_SEND_RICH_INFO** nicht verfügbar ist, folgt der Transportanbieter seinem Standardverhalten, unabhängig davon, was für den jeweiligen Anbieter gilt. 
  
MAPI definiert einen speziellen Eigenschaftentyp, PT_UNSPECIFIED, den ein Client oder Dienstanbieter verwenden kann, um eine Eigenschaft abzurufen, wenn der Eigenschaftentyp unbekannt ist. Um eine Eigenschaft ohne vorherige Kenntnis ihres Typs abzurufen, ruft ein Client oder Dienstanbieter die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) eines Objekts auf und übergibt ein Eigenschaftentag, das aus dem Bezeichner der Eigenschaft und dem PT_UNSPECIFIED-Eigenschaftstyp besteht. **GetProps** gibt eine [SPropValue-Struktur](spropvalue.md) für die Eigenschaft zurück und ersetzt PT_UNSPECIFIED durch den entsprechenden Typ. Dienstanbieter, die **GetProps** implementieren, sind zur Unterstützung von PT_UNSPECIFIED. 
  
Einige MAPI-Objekte unterstützen Eigenschaften, die selbst Objekte sind. Objekteigenschaften haben den Typ PT_OBJECT. Anstatt **IMAPIProp::GetProps** für den Zugriff auf diese Eigenschaften zu verwenden, verwenden Clients und Dienstanbieter in der Regel entweder die [IMAPIProp::OpenProperty-Methode,](imapiprop-openproperty.md) indem sie die entsprechende Schnittstelle für den Zugriff angeben, oder eine Methode für das Objekt, das die Eigenschaft unterstützt. 
  
Da der Zugriff auf den Wert einer Objekteigenschaft die Verwendung einer der Schnittstellen für das Objekt erfordert, **ist GetProps** unangemessen. Mit **GetProps** zugrifft der Aufrufer über eine **SPropValue-Struktur** auf den Wert einer Eigenschaft. Mit **IMAPIProp::OpenProperty** ruft der Aufrufer einen Zeiger auf eine Schnittstelle ab, die auf das Objekt zugreifen kann. **OpenProperty** kann immer zum Abrufen einer Objekteigenschaft verwendet werden. Die andere Option, das Aufrufen einer Methode für das Objekt, ist nicht mit jeder Objekteigenschaft verfügbar. 
  
Jeder Ordner unterstützt beispielsweise zwei Tabellen, eine Hierarchietabelle und eine Inhaltstabelle. Diese Tabellen sind Eigenschaften des Ordners. ihre Eigenschaftstags **sind PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) und **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)). Tabellen sind Objekte, für die die **IMAPITable-Schnittstelle für** den Zugriff erforderlich ist. Ein Client kann die [IMAPIContainer::GetHierarchyTable-Methode](imapicontainer-gethierarchytable.md) des Ordners aufrufen, um auf die Hierarchietabelle, die [IMAPIContainer::GetContentsTable-Methode](imapicontainer-getcontentstable.md) des Ordners für den Zugriff auf die Inhaltstabelle oder die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) des Ordners für den Zugriff auf beide Tabellen zu zugreifen. Zum Aufrufen **von OpenProperty** übergibt ein Client das Eigenschaftstag für die Eigenschaft als ersten Parameter und eine Schnittstellen-ID für die Schnittstelle, die als zweiter Parameter für den Zugriff verwendet werden soll. Diese Parameter werden **PR_CONTAINER_HIERARCHY** oder **PR_CONTAINER_CONTENTS** und **IID_IMAPITable**.
  
Eine vollständige Liste der Eigenschaftentypen mit einem Wert und mehreren Wert finden Sie unter [Property Types](property-types.md). 
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über die MAPI-Eigenschaft](mapi-property-overview.md)

