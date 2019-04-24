---
title: Kanonische Pidtagcontainerflags (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c9c446097213e5b743a47ec32db17ec0afe63b78
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357547"
---
# <a name="pidtagcontainerflags-canonical-property"></a>Kanonische Pidtagcontainerflags (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Bitmaske von Flags, die die Funktionen eines Adressbuch Containers beschreiben. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_CONTAINER_FLAGS  <br/> |
|Kennung:  <br/> |0x3600  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Adressbuch  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Mindestens eines der folgenden Flags kann für die Bitmaske festgelegt werden:
  
AB_FIND_ON_OPEN 
  
> Zeigt ein Dialogfeld an, um eine Einschränkung anzufordern, bevor der Inhalt des Containers angezeigt wird. 
    
AB_MODIFIABLE 
  
> Einträge können dem Container hinzugefügt und daraus entfernt werden. Dieses Flag gibt nicht an, ob Einträge im Container geändert werden können.
    
AB_RECIPIENTS 
  
> Der Container kann Empfänger enthalten. Dieses Flag gibt nicht an, ob Empfänger tatsächlich im Container vorhanden sind oder ob Sie hinzugefügt oder entfernt werden können. 
    
AB_SUBCONTAINERS 
  
> Der Container kann untergeordnete Container enthalten. Dieses Flag gibt nicht an, ob die Untercontainer tatsächlich in dem Behälter vorhanden sind, oder ob Sie hinzugefügt oder entfernt werden können. AB_SUBCONTAINERS muss für den Container für die Unterstützung von [IMAPIContainer:: GetHierarchy](imapicontainer-gethierarchytable.md)festgelegt werden. 
    
AB_UNMODIFIABLE 
  
> Einträge können dem Container nicht hinzugefügt oder daraus entfernt werden. Dieses Flag gibt nicht an, ob Einträge im Container geändert werden können. 
    
Das AB_FIND_ON_OPEN-Flag wird dringend für Container empfohlen, die mit Onlinediensten oder mit langsamen Verbindungen zu Servern verwendet werden. Wenn ein Container geöffnet wird, der AB_FIND_ON_OPEN festgelegt wurde, wird dem Benutzer ein Dialogfeld zum **Suchen** angezeigt, um die angezeigten Messagingbenutzer einzuschränken. Auch eine partielle Spezifikation, die die Messaging-Benutzer beschränkt, kann eine deutliche Beschleunigung der Inhaltsanzeige bedeuten. 
  
Entweder das AB_MODIFIABLE-oder das AB_UNMODIFIABLE-Flag muss festgelegt werden. Beide Flags können festgelegt werden, um anzugeben, dass der Container nicht weiß, ob er geändert werden kann oder nicht, beispielsweise wenn die Änderung von den Zugriffsrechten des Benutzers abhängt. In diesem Fall muss eine Clientanwendung einen Anruf versuchen und den Rückgabecode untersuchen, um die Funktionen des Containers zu ermitteln. Ein Client beginnt in der Regel mit der Untersuchung von AB_MODIFIABLE. Wenn er festgelegt ist, führt der Client einen Aufruf aus, der versucht, den Container zu ändern und den Rückgabewert zu überprüfen. 
  
Das AB_MODIFIABLE-Flag gibt nicht an, welche Typen von Einträgen zum Container hinzugefügt werden können. Um dies zu ermitteln, sollte der Client die entsprechende [OpenProperty](imapiprop-openproperty.md) -Methode verwenden, um die **PR_CREATE_TEMPLATES** ([pidtagcreatetemplates (](pidtagcreatetemplates-canonical-property.md))-Eigenschaft des Containers zu öffnen. Beim Öffnen von **PR_CREATE_TEMPLATES** wird die einmalige Tabelle des Containers zurückgegeben, wobei die Arten von Einträgen aufgelistet werden, die im Container erstellt werden können. 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.
    
[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)
  
> Verarbeitet die Kommunikation eines Clients mit einem NSPI-Server (Name Service Provider Interface).
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

