---
title: PidTagDisplayTypeEx (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayTypeEx
api_type:
- HeaderDef
ms.assetid: 23074402-6ac1-47f1-8a49-b8909f98a26e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 30482f7d6acef7377a1b63bc3de4e43be48d8608
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583358"
---
# <a name="pidtagdisplaytypeex-canonical-property"></a>PidTagDisplayTypeEx (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Enthält den Typ eines Eintrags im Hinblick auf wie der Eintrag für die globale Adressliste in einer Zeile in einer Tabelle angezeigt werden soll. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_DISPLAY_TYPE_EX  <br/> |
|Kennung:  <br/> |0x3905  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Adressbuch  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft gibt den Typ eines Eintrags im Hinblick auf, wie er in der globalen Adressliste angezeigt werden soll. Bietet zusätzliche Informationen, die im **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) dargestellt werden kann.
  
> [!NOTE]
> Die Werte der **PR_DISPLAY_TYPE** und diese Eigenschaft mit "DT_" beginnen und in Mapitags.h definiert sind. Alle Werte, die nicht dokumentiert sind für die MAPI reserviert. Clientanwendungen dürfen Sie keine neue Werte definieren und für den Umgang mit eine nicht dokumentierte Wert vorbereitet sein. 
  
Es gibt einige Makros, die Attribute eines Objekts wie gibt an, ob es sich um lokale, Remote- oder Sicherheit gesteuerte ist bestimmen helfen kann. Diese Makros enthalten: 
  
|**Makro**|**Wert**|
|:-----|:-----|
|DTE_FLAG_REMOTE_VALID  <br/> |0 x 80000000)  <br/> |
|DTE_FLAG_ACL_CAPABLE  <br/> |0 x 40000000  <br/> |
|DTE_MASK_REMOTE  <br/> |0x0000FF00  <br/> |
|DTE_MASK_LOCAL  <br/> |0x000000ff  <br/> |
|DTE_IS_REMOTE_VALID(v)  <br/> |(!! ((V) &amp; DTE_FLAG_REMOTE_VALID)  <br/> |
|DTE_IS_ACL_CAPABLE(v)  <br/> |(!! ((V) &amp; DTE_FLAG_ACL_CAPABLE))  <br/> |
|DTE_REMOTE(v)  <br/> |(((V) &amp; DTE_MASK_REMOTE) \> \> 8)  <br/> |
|DTE_LOCAL(v)  <br/> |((V) &amp; DTE_MASK_LOCAL)  <br/> |
|DT_ROOM  <br/> |((ULONG) 0 X 00000007)  <br/> |
|DT_EQUIPMENT  <br/> |((ULONG) 0 X 00000008)  <br/> |
|DT_SEC_DISTLIST  <br/> |((ULONG) 0X00000009)  <br/> |
   
Es folgen einige Hinweise zur Verwendung dieser Makros. 
  
- Um zu überprüfen, ob ein Eintrag einer remote-Eintrag in einer anderen Gesamtstruktur ist, wenden Sie das Makro DTE_IS_REMOTE_VALID auf den Wert dieser Eigenschaft zu überprüfen, ob das Flag DTE_FLAG_REMOTE_VALID in den Eintrag festgelegt ist. Wenn sie einen remote-Eintrag ist, klicken Sie dann finden, den Typ des remote-Eintrags Sie mithilfe des Makros DTE_REMOTE. 
    
- In einer einzelnen Gesamtstruktur und gesamtstrukturübergreifende Konfigurationen Wenn **PR_DISPLAY_TYPE** hat der Wert der DT_DISTLIST und DTE_IS_REMOTE_VALID false ist, auf den Wert dieser Eigenschaft das Makro DTE_LOCAL angewendet, lassen Sie näher an den Typ des Objekts als DT_DISTLIST (eine Verteilerliste) oder DT_SEC_DISTLIST (einer Verteilerliste Sicherheit). 
    
- Wenn Sie das Makro DTE_LOCAL auf den Wert der **PR_DISPLAY_TYPE_EX** anwenden, und es den Typ DT_REMOTE_MAILUSER gibt, ist der Eintrag einen remote-Eintrag. 
    
- In einer einzelnen Gesamtstruktur oder in einer gesamtstrukturübergreifenden Konfiguration, in dem Replikation durch eine Zugriffssteuerungsliste (ACL) gesteuert wird, können Sie das Makro DTE_IS_ACL_CAPABLE verwenden, um festzustellen, ob ein Eintrag ein Sicherheitsprinzipal ist.
    
In einer Konfiguration gesamtstrukturübergreifenden hat **PR_DISPLAY_TYPE** den Wert des DT_REMOTE_MAILUSER. Anwenden von Makros DTE_REMOTE auf den Wert dieser Eigenschaft können Sie die Abrufen des Typs des remote-Eintrags lassen. Dies sind die möglichen Typen von remote-Eintrag: 
  
|**Typ des Remote-Eintrags**|**Wert**|**Beschreibung**|
|:-----|:-----|:-----|
|DT_AGENT  <br/> |((ULONG) 0 X 00000003)  <br/> |Dynamische Verteilerliste.  <br/> |
|DT_DISTLIST  <br/> |((ULONG) 0 X 00000001)  <br/> |Verteilerliste.  <br/> |
|DT_EQUIPMENT  <br/> |((ULONG) 0 X 00000008)  <br/> |Geräte, beispielsweise einen Drucker oder einen Projektor.  <br/> |
|DT_MAILUSER  <br/> |((ULONG) 0 X 00000000)  <br/> |Benutzer mit einem Postfach.  <br/> |
|DT_REMOTE_MAILUSER  <br/> |((ULONG) 0 X 00000000)  <br/> |Ein Adresseintrag des Liste in der globalen Adressliste.  <br/> |
|DT_ROOM  <br/> |((ULONG) 0 X 00000007)  <br/> |Konferenzraum.  <br/> |
|DT_SEC_DISTLIST  <br/> |((ULONG) 0X00000009)  <br/> |Sicherheit-Verteilerliste.  <br/> |
   
In beiden einer einzelnen Gesamtstruktur und in einem gesamtstrukturübergreifenden Konfiguration, wenn **PR_DISPLAY_TYPE** den Wert der DT_DISTLIST und DTE_IS_REMOTE_VALID hat false ist, das Makro DTE_LOCAL auf den Wert dieser Eigenschaft angewendet, lassen Sie das Abrufen des Typs der Verteilerliste . Dies sind die möglichen Typen der Verteilerliste: 
  
|**Typ der Verteilerliste**|**Wert**|**Beschreibung**|
|:-----|:-----|:-----|
|DT_DISTLIST  <br/> |((ULONG) 0 X 00000001)  <br/> |Verteilerliste.  <br/> |
|DT_SEC_DISTLIST  <br/> |((ULONG) 0X00000009)  <br/> |Sicherheit-Verteilerliste.  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen für Listen der Benutzer, Kontakte, Gruppen und Ressourcen.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

