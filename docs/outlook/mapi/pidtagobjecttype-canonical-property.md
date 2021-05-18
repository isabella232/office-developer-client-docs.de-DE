---
title: PidTagObjectType (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagObjectType
api_type:
- HeaderDef
ms.assetid: 37da4ff5-300d-479f-a8b4-6fc36df997d9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b433db7cb157afbf8c3b506f2ed95b04b7b88564
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329225"
---
# <a name="pidtagobjecttype-canonical-property"></a>PidTagObjectType (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Typ eines Objekts. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_OBJECT_TYPE  <br/> |
|Kennung:  <br/> |0x0FFE  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Standard  <br/> |
   
## <a name="remarks"></a>Hinweise

Der in dieser Eigenschaft enthaltene Objekttyp entspricht der primären Schnittstelle, die für ein Objekt verfügbar ist, auf das über die **OpenEntry-Schnittstelle zugegriffen werden** kann. Sie wird in der Regel durch Rücksprache mit dem  _lpulObjType-Parameter_ ermittelt, der von der entsprechenden **OpenEntry-Methode zurückgegeben** wird. Wenn die Schnittstelle auf andere Weise erhalten wird, rufen [Sie IMAPIProp::GetProps](imapiprop-getprops.md) auf, um den Wert für diese Eigenschaft zu erhalten. 
  
Diese Eigenschaft kann genau einen der folgenden Werte haben:
  
MAPI_ABCONT 
  
> Adressbuchcontainerobjekt 
    
MAPI_ADDRBOOK 
  
> Adressbuchobjekt 
    
MAPI_ATTACH 
  
> Message attachment-Objekt 
    
MAPI_DISTLIST 
  
> Verteilerlistenobjekt 
    
MAPI_FOLDER 
  
> Ordnerobjekt 
    
MAPI_FORMINFO 
  
> Form-Objekt 
    
MAPI_MAILUSER 
  
> Messagingbenutzerobjekt 
    
MAPI_MESSAGE 
  
> Objekt Message 
    
MAPI_PROFSECT 
  
> Profilabschnittsobjekt 
    
MAPI_SESSION 
  
> Session-Objekt 
    
MAPI_STATUS 
  
> Status-Objekt 
    
MAPI_STORE 
  
> Message store-Objekt
    
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.
    
[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)
  
> Verarbeitet die Kommunikation eines Clients mit einem NSPI-Server (Name Service Provider Interface).
    
[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Verarbeitet Ordnervorgänge.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und einem Server.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Konvertiert von Internetstandard-E-Mail-Konventionen in Nachrichtenobjekte.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Behandelt Nachrichten- und Anlagenobjekte.
    
[[MS-OXOAB]](https://msdn.microsoft.com/library/b4750386-66ec-4e69-abb6-208dd131c7de%28Office.15%29.aspx)
  
> Gibt die Offlineadressbuchdateiformate (OAB) für den Cache für lokale Adressbuchobjekte an.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.
    
[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge zum Bearbeiten einer Suchordnerlistenkonfiguration an.
    
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

