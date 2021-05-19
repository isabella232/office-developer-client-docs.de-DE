---
title: PidTagContainerFlags (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContainerFlags
api_type:
- HeaderDef
ms.assetid: 66b8d333-227e-464d-8cf9-cd8a5ff15efb
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c9c446097213e5b743a47ec32db17ec0afe63b78
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357547"
---
# <a name="pidtagcontainerflags-canonical-property"></a>PidTagContainerFlags (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Bitmaske mit Flags, die funktionen eines Adressbuchcontainers beschreiben. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_CONTAINER_FLAGS  <br/> |
|Kennung:  <br/> |0x3600  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Adressbuch  <br/> |
   
## <a name="remarks"></a>Hinweise

Mindestens eines der folgenden Flags kann für die Bitmaske festgelegt werden:
  
AB_FIND_ON_OPEN 
  
> Zeigt ein Dialogfeld an, um eine Einschränkung an fordern, bevor Inhalte des Containers angezeigt werden. 
    
AB_MODIFIABLE 
  
> Einträge können dem Container hinzugefügt und aus dem Container entfernt werden. Dieses Flag gibt nicht an, ob Einträge im Container geändert werden können.
    
AB_RECIPIENTS 
  
> Der Container kann Empfänger enthalten. Dieses Flag gibt nicht an, ob empfänger tatsächlich im Container vorhanden sind oder ob sie hinzugefügt oder entfernt werden können. 
    
AB_SUBCONTAINERS 
  
> Der Container kann untergeordnete Container enthalten. Dieses Flag gibt nicht an, ob subcontainer tatsächlich im Container vorhanden sind oder ob sie hinzugefügt oder entfernt werden können. AB_SUBCONTAINERS muss festgelegt werden, damit der Container [IMAPIContainer::GetHierarchyTable unterstützt.](imapicontainer-gethierarchytable.md) 
    
AB_UNMODIFIABLE 
  
> Einträge können nicht dem Container hinzugefügt oder aus dem Container entfernt werden. Dieses Flag gibt nicht an, ob Einträge im Container geändert werden können. 
    
Das AB_FIND_ON_OPEN wird dringend für Container empfohlen, die mit Onlinediensten oder mit langsamen Verbindungen zu Servern verwendet werden. Wenn ein Container geöffnet wird, AB_FIND_ON_OPEN festgelegt  ist, wird dem Benutzer ein Dialogfeld Suchen angezeigt, um die angezeigten Messagingbenutzer einzuschränken. Selbst eine Teilspezifikation, die die Messagingbenutzer einschränkt, kann die Anzeige der Inhalte erheblich beschleunigen. 
  
Entweder das AB_MODIFIABLE oder AB_UNMODIFIABLE muss festgelegt werden. Beide Flags können so festgelegt werden, dass der Container nicht weiß, ob er geändert werden kann oder nicht, z. B. ob die Änderung von den Zugriffsrechten des Benutzers abhängt. In diesem Fall muss eine Clientanwendung einen Aufruf versuchen und den Rückgabecode untersuchen, um die Funktionen des Containers zu ermitteln. Ein Client beginnt normalerweise mit der AB_MODIFIABLE. Wenn sie festgelegt ist, wird vom Client ein Aufruf ausgeführt, der versucht, den Container zu ändern und den Rückgabewert zu überprüfen. 
  
Das AB_MODIFIABLE gibt nicht an, welche Arten von Einträgen dem Container hinzugefügt werden können. Um dies zu ermitteln, sollte der Client die entsprechende [OpenProperty-Methode](imapiprop-openproperty.md) verwenden, um die **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) -Eigenschaft des Containers zu öffnen. Durch **PR_CREATE_TEMPLATES** wird die einmal erstellte Tabelle des Containers zurückgegeben, in der die Arten von Einträgen aufgeführt werden, die im Container erstellt werden können. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.
    
[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)
  
> Verarbeitet die Kommunikation eines Clients mit einem NSPI-Server (Name Service Provider Interface).
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

