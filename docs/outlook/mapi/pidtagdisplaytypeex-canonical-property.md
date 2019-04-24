---
title: Kanonische PidTagDisplayTypeEx-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 6eea30188543cb06545a9efad705f5593d4227a7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360774"
---
# <a name="pidtagdisplaytypeex-canonical-property"></a>Kanonische PidTagDisplayTypeEx-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Typ eines Eintrags im Hinblick darauf, wie der Eintrag in einer Zeile in einer Tabelle für die globale Adressliste angezeigt werden soll. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_DISPLAY_TYPE_EX  <br/> |
|Kennung:  <br/> |0x3905  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Adressbuch  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft gibt den Typ eines Eintrags an, der angibt, wie er in der globalen Adressliste angezeigt werden soll. Sie bietet zusätzliche Informationen, die in **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) nicht dargestellt werden können.
  
> [!NOTE]
> Die Werte von **PR_DISPLAY_TYPE** und dieser Eigenschaft beginnen mit "dt_" und sind in Mapitags. h definiert. Alle nicht dokumentierten Werte sind für MAPI reserviert. Client Anwendungen dürfen keine neuen Werte definieren und müssen auf den Umgang mit einem nicht dokumentierten Wert vorbereitet sein. 
  
Es gibt einige Makros, die dazu beitragen können, die Attribute eines Objekts zu ermitteln, beispielsweise ob es lokal, Remote oder Sicherheits gesteuert ist. Zu diesen Makros gehört Folgendes: 
  
|**Makro**|**Wert**|
|:-----|:-----|
|DTE_FLAG_REMOTE_VALID  <br/> |0x80000000  <br/> |
|DTE_FLAG_ACL_CAPABLE  <br/> |0x40000000  <br/> |
|DTE_MASK_REMOTE  <br/> |0x0000ff00  <br/> |
|DTE_MASK_LOCAL  <br/> |0x000000ff  <br/> |
|DTE_IS_REMOTE_VALID (v)  <br/> |(!! ((v) &amp; DTE_FLAG_REMOTE_VALID)  <br/> |
|DTE_IS_ACL_CAPABLE (v)  <br/> |(!! ((v) &amp; DTE_FLAG_ACL_CAPABLE))  <br/> |
|DTE_REMOTE (v)  <br/> |(((v) &amp; DTE_MASK_REMOTE \> \> ) 8)  <br/> |
|DTE_LOCAL (v)  <br/> |((v) &amp; DTE_MASK_LOCAL)  <br/> |
|DT_ROOM  <br/> |((ULONG) 0x00000007)  <br/> |
|DT_EQUIPMENT  <br/> |((ULONG) 0x00000008)  <br/> |
|DT_SEC_DISTLIST  <br/> |((ULONG) 0x00000009)  <br/> |
   
Im folgenden finden Sie einige Hinweise zur Verwendung dieser Makros. 
  
- Um zu überprüfen, ob ein Eintrag ein Remote Eintrag in einer anderen Gesamtstruktur ist, wenden Sie das DTE_IS_REMOTE_VALID-Makro auf den Wert dieser Eigenschaft an, um zu überprüfen, ob das DTE_FLAG_REMOTE_VALID-Flag im Eintrag festgelegt ist. Wenn es sich um einen Remote Eintrag handelt, können Sie den Typ des Remote Eintrags mithilfe des DTE_REMOTE-Makros herausfinden. 
    
- Wenn **PR_DISPLAY_TYPE** den Wert DT_DISTLIST und DTE_IS_REMOTE_VALID auf false festgelegt ist, kann das Makro DTE_LOCAL auf den Wert dieser Eigenschaft angewendet werden, um den Typ des Objekts weiter zu identifizieren, wenn entweder DT_DISTLIST (eine Verteilerliste) oder DT_SEC_DISTLIST (eine Sicherheits Verteilerliste). 
    
- Wenn Sie das Makro DTE_LOCAL auf den Wert von **PR_DISPLAY_TYPE_EX** anwenden und den Typ DT_REMOTE_MAILUSER zurückgibt, handelt es sich bei dem Eintrag um einen Remote Eintrag. 
    
- In einer einzelnen Gesamtstruktur oder in einer gesamtstrukturübergreifenden Konfiguration, bei der die Replikation durch eine Zugriffssteuerungsliste (Access Control List, ACL) gesteuert wird, können Sie mithilfe des DTE_IS_ACL_CAPABLE-Makros ermitteln, ob ein Eintrag ein Sicherheitsprinzipal ist.
    
Bei einer gesamtstrukturübergreifenden Konfiguration besitzt **PR_DISPLAY_TYPE** den Wert von DT_REMOTE_MAILUSER. Wenn Sie das Makro DTE_REMOTE auf den Wert dieser Eigenschaft anwenden, können Sie den Typ des Remote Eintrags abrufen. Folgende Arten von Remote Einträgen sind möglich: 
  
|**Typ des Remote Eintrags**|**Wert**|**Beschreibung**|
|:-----|:-----|:-----|
|DT_AGENT  <br/> |((ULONG) 0x00000003)  <br/> |Dynamische Verteilerliste.  <br/> |
|DT_DISTLIST  <br/> |((ULONG) 0x00000001)  <br/> |Verteilerliste.  <br/> |
|DT_EQUIPMENT  <br/> |((ULONG) 0x00000008)  <br/> |Geräte, beispielsweise einen Drucker oder einen Projektor.  <br/> |
|DT_MAILUSER  <br/> |((ULONG) 0x00000000)  <br/> |Benutzer mit einem Postfach.  <br/> |
|DT_REMOTE_MAILUSER  <br/> |((ULONG) 0x00000000)  <br/> |Ein Adresslisten Eintrag in der globalen Adressliste.  <br/> |
|DT_ROOM  <br/> |((ULONG) 0x00000007)  <br/> |Konferenzraum.  <br/> |
|DT_SEC_DISTLIST  <br/> |((ULONG) 0x00000009)  <br/> |Sicherheits Verteilerliste.  <br/> |
   
In einer einzelnen Gesamtstruktur und in einer gesamtstrukturübergreifenden Konfiguration, wenn **PR_DISPLAY_TYPE** den Wert DT_DISTLIST und DTE_IS_REMOTE_VALID ist false ist, kann Anwenden des DTE_LOCAL-Makros auf den Wert dieser Eigenschaft können Sie den Typ der Verteilerliste abrufen . Folgende Arten von Verteilerlisten sind möglich: 
  
|**Typ der Verteilerliste**|**Wert**|**Beschreibung**|
|:-----|:-----|:-----|
|DT_DISTLIST  <br/> |((ULONG) 0x00000001)  <br/> |Verteilerliste.  <br/> |
|DT_SEC_DISTLIST  <br/> |((ULONG) 0x00000009)  <br/> |Sicherheits Verteilerliste.  <br/> |
   
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

