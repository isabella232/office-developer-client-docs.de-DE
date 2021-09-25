---
title: PidTagRpcOverHttpFlags (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: c8b30768-cf83-450d-9fe2-567a5e0c2f57
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5f875db0d814722c8a9901b54c071dfd1ffdabfa
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59604222"
---
# <a name="pidtagrpcoverhttpflags-canonical-property"></a>PidTagRpcOverHttpFlags (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die Einstellungen in einem Profil, das von Microsoft Office Outlook zum Herstellen einer Verbindung mit Microsoft Exchange Server mithilfe eines Remoteprozeduraufrufs (RPC) über http (Hypertext Transfer Protocol) verwendet wird.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ROH_FLAGS  <br/> |
|Kennung:  <br/> |0x6623  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Sonstiges  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Die **PR_ROH_FLAGS-Eigenschaft** wird im Abschnitt "Globales Profil" eines MAPI-Profils (Messaging Application Programming Interface) gespeichert. Der Wert von **PR_ROH_FLAGS** ist eine Bitmaske, die aus einem oder mehreren der folgenden Flags besteht. 
  
|**Name**|**Wert**|**Beschreibung**|
|:-----|:-----|:-----|
|**ROHFLAGS_USE_ROH** <br/> |0x1  <br/> |Verbinden mithilfe von RPC über HTTP zum Exchange Server.  <br/> |
|**ROHFLAGS_SSL_ONLY** <br/> |0x2  <br/> |Verbinden nur mit Secure Socket Layer (SSL) zum Exchange Server.  <br/> |
|**ROHFLAGS_MUTUAL_AUTH** <br/> |0x4  <br/> |Authentifizieren Sie die Sitzung bei der Verbindung mit SSL gegenseitig.  <br/> |
|**ROHFLAGS_HTTP_FIRST_ON_FAST** <br/> |0x8  <br/> |Stellen Sie in schnellen Netzwerken zuerst eine Verbindung mithilfe von HTTP her. Stellen Sie dann eine Verbindung mithilfe von TCP/IP her.  <br/> |
|**ROHFLAGS_HTTP_FIRST_ON_SLOW** <br/> |0x20  <br/> |Stellen Sie in langsamen Netzwerken zuerst eine Verbindung mithilfe von HTTP her. Stellen Sie dann eine Verbindung mithilfe von TCP/IP her.  <br/> |
   
Um beispielsweise die **PR_ROH_FLAGS-Eigenschaft** so festzulegen, dass RPC über HTTP aktiviert wird, SSL erforderlich ist und um anzugeben, dass das HTTP-Protokoll zuerst für langsame Verbindungen verwendet werden soll, legen Sie den Wert der **PR_ROH_FLAGS-Eigenschaft**  `ROHFLAGS_USE_ROH | ROHFLAGS_SSL_ONLY | ROHFLAGS_HTTP_FIRST_ON_SLOW` fest, die 0x23 entspricht. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Definiert die grundlegenden Datenstrukturen, die in Remotevorgängen verwendet werden.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.
    
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

