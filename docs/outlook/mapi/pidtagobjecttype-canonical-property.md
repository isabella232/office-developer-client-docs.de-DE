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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 2830da6aad561045a7ecdd953286c90edea88ca2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794653"
---
# <a name="pidtagobjecttype-canonical-property"></a>PidTagObjectType (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Enthält den Typ eines Objekts. 
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_OBJECT_TYPE  <br/> |
|Bezeichner:  <br/> |0x0FFE  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Common  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der in dieser Eigenschaft enthaltenen Objekttyp entspricht die primäre Schnittstelle für ein Objekt kann über die Schnittstelle **OpenEntry** zugegriffen werden. Es wird in der Regel durch consulting des _LpulObjType_ -Parameters der entsprechenden **OpenEntry** -Methode zurückgegebene abgerufen. Wenn die Schnittstelle auf andere Weise abgerufen wird, rufen Sie [IMAPIProp::GetProps](imapiprop-getprops.md) , um den Wert für diese Eigenschaft zu erhalten. 
  
Diese Eigenschaft kann genau einen der folgenden Werte aufweisen:
  
MAPI_ABCONT 
  
> Address Book Container-Objekt 
    
MAPI_ADDRBOOK 
  
> Address Book-Objekt 
    
MAPI_ATTACH 
  
> Nachricht Attachment-Objekt 
    
MAPI_DISTLIST 
  
> Verteilung List-Objekt 
    
MAPI_FOLDER 
  
> Folder-Objekt 
    
MAPI_FORMINFO 
  
> Form-Objekt 
    
MAPI_MAILUSER 
  
> Messaging-Benutzerobjekt 
    
MAPI_MESSAGE 
  
> Objekt Message 
    
MAPI_PROFSECT 
  
> Profil Section-Objekt 
    
MAPI_SESSION 
  
> Session-Objekt 
    
MAPI_STATUS 
  
> Statusobjekt 
    
MAPI_STORE 
  
> Objekt "Message" store
    
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen für Listen der Benutzer, Kontakte, Gruppen und Ressourcen.
    
[[MS-NSPI]](http://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)
  
> Verarbeitet ein Client-Kommunikation mit einem Server (NSPI = Name Service Provider Interface).
    
[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Ordner Vorgänge behandelt.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und Server.
    
[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Konvertiert von Internet-standard-e-Mail-Konventionen in Message-Objekten.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Nachrichten und Anlagen Objekte behandelt.
    
[[MS-OXOAB]](http://msdn.microsoft.com/library/b4750386-66ec-4e69-abb6-208dd131c7de%28Office.15%29.aspx)
  
> Gibt die Offlineadressbuch Offlineadressbuch (OAB)-Dateiformate für den lokalen Adresse Adressbuch Objektcache an.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.
    
[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen für das Bearbeiten der Liste einer Suchkonfiguration-Ordner.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

