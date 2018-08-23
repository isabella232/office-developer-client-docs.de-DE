---
title: Konstruieren von Eintragsbezeichnern
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bc2a9116-948e-4da3-96b8-26d73bcd63c4
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f15749077596bd6c89828eb730cadd5624a75fe1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564584"
---
# <a name="constructing-entry-identifiers"></a>Konstruieren von Eintragsbezeichnern

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Eintragsbezeichner werden mit der [ENTRYID](entryid.md) -Struktur erstellt. Die **ENTRYID** -Struktur besteht ein Flag, das die Attribute des Eintrags-ID und die tatsächlichen Eintrags-ID beschreibt. 
  
## <a name="entryid-structure"></a>ENTRYID-Struktur

Die **ENTRYID** -Struktur ist wie folgt definiert: 
  
```cpp
typedef struct
{
    BYTE        abFlags[4];
    BYTE        ab[MAPI_DIM];
}  ENTRYID, FAR *LPENTRYID;
 
```

MAPI_DIM ist eine Konstante, die in der Headerdatei MapiDefs.h definiert ist. 
  
Das erste Byte des Elements 4-Byte- **AbFlags** beschreibt die Art und Verwendung der Eintrags-ID und kann die folgenden Werte aufweisen: 
  
- MAPI_NOTRECI – Gibt an, dass die Eintrags-ID kann nicht als Empfänger einer Nachricht verwendet werden.
    
- MAPI_NOTRESERVED – Gibt an, dass andere Benutzer die Eintrags-ID zugreifen können.
    
- MAPI_NOW – Gibt an, dass die Eintrags-ID in anderen Fällen nicht verwendet werden kann.
    
- MAPI_SHORTTERM – Gibt an, dass die Eintrags-ID kurzfristige ist. Alle anderen Werte in dieses Byte müssen festgelegt werden, es sei denn, weitere Verwendungsmöglichkeiten des Bezeichners Eintrag zulässig sind.
    
- MAPI_THISSESSION – Gibt an, dass die Eintrags-ID für andere-Sitzungen verwendet werden kann.
    
- MAPI_NOTRESERVED – Gibt an, dass die Eintrags-ID für andere Objekte von anderen Dienstanbietern verwendet werden kann.
    
Das **Ab** Element Eintragsbezeichner, die Zeichenfolgeneigenschaften Address Book und Nachricht erstellt wird besteht aus zwei Teilen: eine 16-Byte- [MAPIUID](mapiuid.md) -Struktur, die der Dienstanbieter und ein Inhaltselement, um das Objekt zu identifizieren identifiziert. **MAPIUID** ist eine Struktur, die einen global eindeutigen Bezeichner oder eine GUID enthält. Eine GUID ist eine Byte-Reihenfolge-unabhängigen-ID, die erstellt werden können, mit der Microsoft Visual Studio-*GUID erstellen** Tool. 
  
Ein Dienstanbieter registriert seine **MAPIUID** Struktur mit MAPI während des Anmeldevorgangs in einem Aufruf der [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) -Methode. Wenn ein Client eine Methode **OpenEntry** Zugriff auf ein Objekt aufruft, verwendet MAPI die **MAPIUID** -Struktur, um zu bestimmen, welcher Dienst Anbieter, dass der Zugriff bereitstellen kann. Dienstanbieter sollten die gleiche **MAPIUID** -Struktur für alle Versionen von ihrer DLL verwenden. Auf diese Weise können Clients durch die neuere Version Antworten auf Nachrichten gesendet und mit der älteren Version gespeichert. 
  
Der Rest des Elements **Ab** , nachdem die 16-Byte- **MAPIUID** Service-anbieterspezifische Binärdaten zum Identifizieren von bestimmter Objekten enthält. Es ist keine fester Größe für dieses Teils des Eintrags-ID ein. Beliebiger Größe innerhalb Grund kann sein. Ein Dienstanbieter umfasst in der Regel die folgende Informationen in diesem Teil seiner Eintragsbezeichner: 
  
- Versionsinformationen –, da es für einen Dienstanbieter, ändern Sie das Format der seine Eintragsbezeichner von Version zu Version üblich ist, Speichern von Informationen zur Version ermöglicht schnell ermitteln, wie Sie eine beliebige Eintrags-ID zu entschlüsseln.
    
- Standortinformationen – Standortinformationen sind Daten, die einem Dienstanbieter ein Symbol zum Objekt dargestellt durch die Eintrags-ID gefunden werden können. Beispielsweise kann ein Dienstanbieter bewahren Sie die Diskette offset für die letzte Stelle in einer Datendatei, dass das Objekt gespeichert wurde. Da diese Art von Informationen mit der Zeit ändern kann, sollten Dienstanbieter für die Suche nach Objekten in ihren Eintragsbezeichner verschiedene Arten bereitstellen.
    
Zwar Dienstanbieter ihre Eintragsbezeichner wiederverwendet werden können, sollten sie dieses Verfahren vermeiden. Wenn es eine Eintrags-ID wiederverwenden erforderlich ist, sollten-Dienstanbieter den Zeitraum an, die verstreicht, zwischen dem zum ersten Mal verwenden und die Wiederverwendung so lange wie möglich. Darüber hinaus sollten die Eintrags-ID in ein anderes Objekt des gleichen Typs neu zugewiesen werden. D. h., sollte ein bestimmten Eintrag Bezeichner nicht zuerst mit einer Meldung, und klicken Sie dann mit einem Ordner verknüpft sein.
  
## <a name="see-also"></a>Siehe auch



[MAPI-Eintragsbezeichner](mapi-entry-identifiers.md)

