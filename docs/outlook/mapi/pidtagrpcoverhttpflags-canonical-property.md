---
title: Kanonische Pidtagrpcoverhttpflags (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c8b30768-cf83-450d-9fe2-567a5e0c2f57
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: cf1f3b4d72426fb5f80decdc074a622b140657c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327447"
---
# <a name="pidtagrpcoverhttpflags-canonical-property"></a>Kanonische Pidtagrpcoverhttpflags (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die Einstellungen in einem Profil, das von Microsoft Office Outlook zum Herstellen einer Verbindung mit Microsoft Exchange Server mithilfe eines Remoteprozeduraufrufs (RPC) über Hypertext Transfer Protocol (HTTP) verwendet wird.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ROH_FLAGS  <br/> |
|Kennung:  <br/> |0x6623  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Sonstiges  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die **PR_ROH_FLAGS** -Eigenschaft wird im Abschnitt globaler Profil eines MAPI-Profils (Messaging Application Programming Interface) gespeichert. Der Wert von **PR_ROH_FLAGS** ist eine Bitmaske, die aus einem oder mehreren der folgenden Flags besteht. 
  
|**Name**|**Wert**|**Beschreibung**|
|:-----|:-----|:-----|
|**ROHFLAGS_USE_ROH** <br/> |0x1  <br/> |Stellen Sie über RPC über HTTP eine Verbindung mit dem Exchange-Server her.  <br/> |
|**ROHFLAGS_SSL_ONLY** <br/> |0x2  <br/> |Stellen Sie eine Verbindung mit dem Exchange-Server nur über Secure Sockets Layer (SSL) her.  <br/> |
|**ROHFLAGS_MUTUAL_AUTH** <br/> |0x4  <br/> |Die Sitzung gegenseitig authentifizieren, wenn eine Verbindung über SSL hergestellt wird.  <br/> |
|**ROHFLAGS_HTTP_FIRST_ON_FAST** <br/> |0x8  <br/> |Stellen Sie in schnellen Netzwerken zuerst eine Verbindung über HTTP her. Stellen Sie dann eine Verbindung über TCP/IP her.  <br/> |
|**ROHFLAGS_HTTP_FIRST_ON_SLOW** <br/> |0x20  <br/> |Stellen Sie in langsamen Netzwerken zuerst eine Verbindung über HTTP her. Stellen Sie dann eine Verbindung über TCP/IP her.  <br/> |
   
Wenn Sie beispielsweise festlegen möchten, dass die **PR_ROH_FLAGS** -Eigenschaft RPC über HTTP aktivieren muss, um SSL zu erfordern, und um anzugeben, dass das HTTP-Protokoll zuerst bei langsamen Verbindungen verwendet werden soll, legen `ROHFLAGS_USE_ROH | ROHFLAGS_SSL_ONLY | ROHFLAGS_HTTP_FIRST_ON_SLOW` Sie den Wert der **PR_ROH_FLAGS** -Eigenschaft auf, die gleich 0x23 ist. 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Definiert die grundlegenden Datenstrukturen, die in Remotevorgängen verwendet werden.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für e-Mail-Nachrichtenobjekte zulässig sind.
    
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

