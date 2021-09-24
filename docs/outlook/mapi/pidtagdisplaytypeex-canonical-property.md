---
title: PidTagDisplayTypeEx (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagDisplayTypeEx
api_type:
- HeaderDef
ms.assetid: 23074402-6ac1-47f1-8a49-b8909f98a26e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3a40e4c8a7a4380304e57998b8f54a209f463bf9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550694"
---
# <a name="pidtagdisplaytypeex-canonical-property"></a>PidTagDisplayTypeEx (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Typ eines Eintrags im Hinblick darauf, wie der Eintrag in einer Zeile in einer Tabelle für die globale Adressliste angezeigt werden soll. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_DISPLAY_TYPE_EX  <br/> |
|Kennung:  <br/> |0x3905  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Adressbuch  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft gibt den Typ eines Eintrags im Hinblick darauf an, wie er in der globalen Adressliste angezeigt werden soll. Es stellt zusätzliche Informationen bereit, die nicht in **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) dargestellt werden können.
  
> [!NOTE]
> Die Werte von **PR_DISPLAY_TYPE** und dieser Eigenschaft beginnen mit "DT_" und werden in Mapitags.h definiert. Alle nicht dokumentierten Werte sind für DIE MAPI reserviert. Clientanwendungen dürfen keine neuen Werte definieren und müssen darauf vorbereitet sein, mit einem undokumentierten Wert umzugehen. 
  
Es gibt einige Makros, die helfen können, Attribute eines Objekts zu bestimmen, z. B. ob es lokal, remote oder sicherheitsgesteuert ist. Zu diesen Makros gehören: 
  
|**Makro**|**Wert**|
|:-----|:-----|
|DTE_FLAG_REMOTE_VALID  <br/> |0x80000000)  <br/> |
|DTE_FLAG_ACL_CAPABLE  <br/> |0x40000000  <br/> |
|DTE_MASK_REMOTE  <br/> |0x0000ff00  <br/> |
|DTE_MASK_LOCAL  <br/> |0x000000ff  <br/> |
|DTE_IS_REMOTE_VALID(v)  <br/> |(!! ((v) &amp; DTE_FLAG_REMOTE_VALID)  <br/> |
|DTE_IS_ACL_CAPABLE(v)  <br/> |(!! ((v) &amp; DTE_FLAG_ACL_CAPABLE))  <br/> |
|DTE_REMOTE(v)  <br/> |((v) &amp; DTE_MASK_REMOTE) \> \> 8)  <br/> |
|DTE_LOCAL(v)  <br/> |((v) &amp; DTE_MASK_LOCAL)  <br/> |
|DT_ROOM  <br/> |((ULONG) 0x00000007)  <br/> |
|DT_EQUIPMENT  <br/> |((ULONG) 0x00000008)  <br/> |
|DT_SEC_DISTLIST  <br/> |((ULONG) 0x00000009)  <br/> |
   
Im Folgenden finden Sie einige Hinweise zur Verwendung dieser Makros. 
  
- Um zu überprüfen, ob es sich bei einem Eintrag um einen Remoteeintrag in einer anderen Gesamtstruktur handelt, wenden Sie das makro DTE_IS_REMOTE_VALID auf den Wert dieser Eigenschaft an, um zu überprüfen, ob das DTE_FLAG_REMOTE_VALID Flag im Eintrag festgelegt ist. Wenn es sich um einen Remoteeintrag handelt, können Sie den Typ des Remoteeintrags mithilfe des Makros DTE_REMOTE ermitteln. 
    
- Wenn PR_DISPLAY_TYPE den Wert DT_DISTLIST hat und **DTE_IS_REMOTE_VALID** "false" ist, können Sie bei Konfigurationen mit einer einzelnen Gesamtstruktur und gesamtstrukturübergreifenden Konfigurationen den Typ des Objekts durch Anwenden des Makros DTE_LOCAL auf den Wert dieser Eigenschaft weiter als DT_DISTLIST (Verteilerliste) oder DT_SEC_DISTLIST (Sicherheitsverteilungsliste) identifizieren. 
    
- Wenn Sie das Makro DTE_LOCAL auf den Wert von **PR_DISPLAY_TYPE_EX** anwenden und den Typ DT_REMOTE_MAILUSER zurückgeben, ist der Eintrag ein Remoteeintrag. 
    
- In einer einzelnen Gesamtstruktur oder in einer gesamtstrukturübergreifenden Konfiguration, bei der die Replikation durch eine Zugriffssteuerungsliste (Access Control List, ACL) gesteuert wird, können Sie mithilfe des makros DTE_IS_ACL_CAPABLE bestimmen, ob ein Eintrag ein Sicherheitsprinzipal ist.
    
In einer gesamtstrukturübergreifenden Konfiguration hat **PR_DISPLAY_TYPE** den Wert DT_REMOTE_MAILUSER. Wenn Sie das Makro DTE_REMOTE auf den Wert dieser Eigenschaft anwenden, können Sie den Typ des Remoteeintrags abrufen. Die folgenden Remoteeingabetypen sind möglich: 
  
|**Typ des Remoteeintrags**|**Wert**|**Beschreibung**|
|:-----|:-----|:-----|
|DT_AGENT  <br/> |((ULONG) 0x00000003)  <br/> |Dynamische Verteilerliste.  <br/> |
|DT_DISTLIST  <br/> |((ULONG) 0x00000001)  <br/> |Verteilerliste.  <br/> |
|DT_EQUIPMENT  <br/> |((ULONG) 0x00000008)  <br/> |Geräte, z. B. Drucker oder Projektor.  <br/> |
|DT_MAILUSER  <br/> |((ULONG) 0x00000000)  <br/> |Benutzer mit einem Postfach.  <br/> |
|DT_REMOTE_MAILUSER  <br/> |((ULONG) 0x00000000)  <br/> |Ein Adresslisteneintrag in der globalen Adressliste.  <br/> |
|DT_ROOM  <br/> |((ULONG) 0x00000007)  <br/> |Konferenzraum.  <br/> |
|DT_SEC_DISTLIST  <br/> |((ULONG) 0x00000009)  <br/> |Sicherheitsverteilungsliste.  <br/> |
   
Wenn **PR_DISPLAY_TYPE** sowohl in einer einzelnen Gesamtstruktur als auch in einer gesamtstrukturübergreifenden Konfiguration den Wert DT_DISTLIST hat und DTE_IS_REMOTE_VALID auf "false" festgelegt ist, können Sie durch Anwenden des makros DTE_LOCAL auf den Wert dieser Eigenschaft den Typ der Verteilerliste abrufen. Die folgenden Arten von Verteilerlisten sind möglich: 
  
|**Typ der Verteilerliste**|**Wert**|**Beschreibung**|
|:-----|:-----|:-----|
|DT_DISTLIST  <br/> |((ULONG) 0x00000001)  <br/> |Verteilerliste.  <br/> |
|DT_SEC_DISTLIST  <br/> |((ULONG) 0x00000009)  <br/> |Sicherheitsverteilungsliste.  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

