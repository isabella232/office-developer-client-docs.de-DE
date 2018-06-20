---
title: Kanonische PidTagRpcOverHttpFlags-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c8b30768-cf83-450d-9fe2-567a5e0c2f57
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 151aa730f2ae6a4d39ffa474eb7ecd79ed5602eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794989"
---
# <a name="pidtagrpcoverhttpflags-canonical-property"></a>Kanonische PidTagRpcOverHttpFlags-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Enthält die Einstellungen in einem Profil von Microsoft Office Outlook verwendet werden, um mit Microsoft Exchange Server eine Verbindung über einen Remoteprozeduraufruf (RPC) über Hypertext Transfer Protocol (HTTP).
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_ROH_FLAGS  <br/> |
|Bezeichner:  <br/> |0x6623  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Verschiedenes  <br/> |
   
## <a name="remarks"></a>Hinweise

Die **PR_ROH_FLAGS** -Eigenschaft wird im Abschnitt globale Profil ein Profil Messaging Application Programming Interface (MAPI) gespeichert. Der Wert der **PR_ROH_FLAGS** ist eine Bitmaske, die von einem oder mehreren der folgenden Werte bestehen. 
  
|**Name**|**Wert**|**Beschreibung**|
|:-----|:-----|:-----|
|**ROHFLAGS_USE_ROH** <br/> |0 x 1  <br/> |Verbinden Sie mit dem Exchange-Server mit RPC über HTTP.  <br/> |
|**ROHFLAGS_SSL_ONLY** <br/> |0 x 2  <br/> |Verbinden Sie mit dem Exchange-Server nur über Secure Socket Layer (SSL).  <br/> |
|**ROHFLAGS_MUTUAL_AUTH** <br/> |0 x 4  <br/> |Sitzung gegenseitig authentifizieren beim Herstellen einer Verbindung mit SSL.  <br/> |
|**ROHFLAGS_HTTP_FIRST_ON_FAST** <br/> |0 x 8  <br/> |Bei schnellen Netzwerken zuerst eine Verbindung über HTTP. Verbinden Sie dann mithilfe von TCP/IP.  <br/> |
|**ROHFLAGS_HTTP_FIRST_ON_SLOW** <br/> |0 x 20  <br/> |Bei langsamen Netzwerken zuerst eine Verbindung über HTTP. Verbinden Sie dann mithilfe von TCP/IP.  <br/> |
   
Beispielsweise die **PR_ROH_FLAGS** festgelegt einschalten RPC über HTTP, SSL erforderlich ist, und um anzugeben, dass das HTTP-Protokoll zuerst bei langsamer Verbindung verwendet werden soll Eigenschaftensatz-den Wert der Eigenschaft **PR_ROH_FLAGS** `ROHFLAGS_USE_ROH | ROHFLAGS_SSL_ONLY | ROHFLAGS_HTTP_FIRST_ON_SLOW` gleich 0 x 23 ist. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Definiert die grundlegende Datenstrukturen, die verwendet werden remote-Vorgängen.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.
    
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

