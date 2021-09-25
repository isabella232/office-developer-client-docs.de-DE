---
title: PidTagContainerFlags (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagContainerFlags
api_type:
- HeaderDef
ms.assetid: 66b8d333-227e-464d-8cf9-cd8a5ff15efb
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8816d3cbb4c34330cdc970f1d197aeda415f9ed2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600372"
---
# <a name="pidtagcontainerflags-canonical-property"></a>PidTagContainerFlags (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Bitmaske mit Flags, die die Funktionen eines Adressbuchcontainers beschreiben. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_CONTAINER_FLAGS  <br/> |
|Kennung:  <br/> |0x3600  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Adressbuch  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Mindestens eines der folgenden Flags kann für die Bitmaske festgelegt werden:
  
AB_FIND_ON_OPEN 
  
> Zeigt ein Dialogfeld zum Anfordern einer Einschränkung an, bevor Der Inhalt des Containers angezeigt wird. 
    
AB_MODIFIABLE 
  
> Einträge können dem Container hinzugefügt und daraus entfernt werden. Dieses Flag gibt nicht an, ob Einträge im Container geändert werden können.
    
AB_RECIPIENTS 
  
> Der Container kann Empfänger enthalten. Dieses Flag gibt nicht an, ob Empfänger tatsächlich im Container vorhanden sind oder ob sie hinzugefügt oder entfernt werden können. 
    
AB_SUBCONTAINERS 
  
> Der Container kann untergeordnete Container enthalten. Dieses Flag gibt weder an, ob subcontainers tatsächlich im Container vorhanden sind, noch ob sie hinzugefügt oder entfernt werden können. AB_SUBCONTAINERS muss festgelegt werden, damit der Container [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md)unterstützt. 
    
AB_UNMODIFIABLE 
  
> Einträge können dem Container nicht hinzugefügt oder daraus entfernt werden. Dieses Flag gibt nicht an, ob Einträge im Container geändert werden können. 
    
Das flag AB_FIND_ON_OPEN wird dringend für Container empfohlen, die mit Onlinediensten oder langsamen Verbindungen mit Servern verwendet werden. Wenn ein Container geöffnet wird, für den AB_FIND_ON_OPEN festgelegt ist, wird dem Benutzer ein Dialogfeld **"Suchen"** angezeigt, um die angezeigten Messagingbenutzer einzuschränken. Selbst eine partielle Spezifikation, die die Messaging-Benutzer einschränkt, kann die Anzeige der Inhalte erheblich beschleunigen. 
  
Entweder muss das AB_MODIFIABLE- oder AB_UNMODIFIABLE-Kennzeichen festgelegt werden. Beide Flags können so festgelegt werden, dass der Container nicht weiß, ob er geändert werden kann oder nicht, z. B. wenn die Änderung von den Zugriffsrechten des Benutzers abhängt. In diesem Fall muss eine Clientanwendung einen Aufruf versuchen und den Rückgabecode überprüfen, um die Funktionen des Containers zu ermitteln. Ein Client beginnt in der Regel mit der Untersuchung AB_MODIFIABLE. Wenn er festgelegt ist, führt der Client einen Aufruf durch, der versucht, den Container zu ändern, und überprüft den Rückgabewert. 
  
Das flag AB_MODIFIABLE gibt nicht an, welche Arten von Einträgen dem Container hinzugefügt werden können. Um dies zu ermitteln, sollte der Client die entsprechende [OpenProperty-Methode](imapiprop-openproperty.md) verwenden, um die **eigenschaft PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) des Containers zu öffnen. Beim Öffnen **PR_CREATE_TEMPLATES** wird die einmalige Tabelle des Containers zurückgegeben, wobei die Arten von Einträgen aufgelistet werden, die im Container erstellt werden können. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.
    
[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)
  
> Verarbeitet die Kommunikation eines Clients mit einem NSPI-Server (Name Service Provider Interface).
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

