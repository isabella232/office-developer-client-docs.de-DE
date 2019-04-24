---
title: Erstellen von Eintrags Bezeichnern
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bc2a9116-948e-4da3-96b8-26d73bcd63c4
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8d48c2584fa5b7e862102e401ea8165821607f77
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335091"
---
# <a name="constructing-entry-identifiers"></a>Erstellen von Eintrags Bezeichnern

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eintragsbezeichner werden mit der [Eintrags](entryid.md) -ID-Struktur erstellt. Die **Eintrags** -ID-Struktur besteht aus einem Flag, das die Attribute des Eintrags Bezeichners und des tatsächlichen Eintrags Bezeichners beschreibt. 
  
## <a name="entryid-structure"></a>EINTRAGs-Struktur

Die **Eintrags** -Struktur ist wie folgt definiert: 
  
```cpp
typedef struct
{
    BYTE        abFlags[4];
    BYTE        ab[MAPI_DIM];
}  ENTRYID, FAR *LPENTRYID;
 
```

MAPI_DIM ist eine Konstante, die in der Headerdatei MapiDefs. h definiert ist. 
  
Das erste Byte des 4-Byte- **abFlags** -Elements beschreibt den Typ und die Verwendung des Eintrags Bezeichners und kann die folgenden Werte aufweisen: 
  
- MAPI_NOTRECI – gibt an, dass die Eintrags-ID nicht als Empfänger für eine Nachricht verwendet werden kann.
    
- MAPI_NOTRESERVED – gibt an, dass andere Benutzer nicht auf die Eintrags-ID zugreifen können.
    
- MAPI_NOW – gibt an, dass die Eintrags-ID nicht zu anderen Zeiten verwendet werden kann.
    
- MAPI_SHORTTERM – gibt an, dass die Eintrags-ID kurzfristig ist. Alle anderen Werte in diesem Byte müssen festgelegt werden, es sei denn, andere Verwendungen der Eintrags-ID sind zulässig.
    
- MAPI_THISSESSION – gibt an, dass die Eintrags-ID nicht in anderen Sitzungen verwendet werden kann.
    
- MAPI_NOTRESERVED – gibt an, dass die Eintrags-ID von anderen Dienstanbietern für andere Objekte verwendet werden kann.
    
Das **ab** -Element von Eintrags-IDs, das von Adressbuch-und Nachrichtenspeicher Anbietern erstellt wird, besteht aus zwei Teilen: eine 16-Byte- [MAPIUID](mapiuid.md) -Struktur, die den Dienstanbieter identifiziert, und ein Stück zur Identifizierung des Objekts. **MAPIUID** ist eine Struktur, die einen global eindeutigen Bezeichner oder eine GUID enthält. Eine GUID ist ein Bytereihenfolge-unabhängiger Bezeichner, der mithilfe des Microsoft Visual Studio*Create GUID**-Tools erstellt werden kann. 
  
Ein Dienstanbieter registriert seine **MAPIUID** -Struktur während des Anmeldevorgangs bei einem Aufruf der [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md) -Methode mit MAPI. Wenn ein Client eine **OpenEntry** -Methode für den Zugriff auf ein Objekt aufruft, bestimmt MAPI mithilfe der **MAPIUID** -Struktur, welcher Dienstanbieter diesen Zugriff bereitstellen kann. Dienstanbieter sollten dieselbe **MAPIUID** -Struktur für alle Versionen Ihrer dll verwenden. Auf diese Weise können Clients mit der neueren Version auf Nachrichten Antworten, die mit der älteren Version gesendet und gespeichert wurden. 
  
Der Rest des **ab** -Elements nach der 16-Byte- **MAPIUID** enthält Dienstanbieter spezifische Binärdaten zum Identifizieren bestimmter Objekte. Für diesen Teil der Eintrags-ID gibt es keine feste Größe. Es kann eine beliebige Größe innerhalb der Grund sein. Ein Dienstanbieter enthält in der Regel die folgenden Informationen in diesem Teil seiner Eintrags-IDs: 
  
- Versionsinformationen – da es für einen Dienstanbieter üblich ist, das Format seiner Eintrags-IDs von Version zu Version zu ändern, ermöglicht das Speichern von Versionsinformationen, schnell festzustellen, wie jeder Eintragsbezeichner entschlüsselt werden kann.
    
- Standortinformationen – Speicherortinformationen sind Daten, die einem Dienstanbieter einen Indikator für das Auffinden des durch die Eintrags-ID dargestellten Objekts geben. Ein Dienstanbieter kann beispielsweise den Datenträger Offset für die letzte Position in einer Datendatei speichern, die das Objekt gespeichert wurde. Da diese Art von Informationen sich im Lauf der Zeit ändern kann, sollten Dienstanbieter mehrere Möglichkeiten bieten, Objekte in ihren Eintrags Bezeichnern zu suchen.
    
Obwohl Dienstanbieter Ihre Eintrags-IDs wieder verwenden können, sollten Sie diese Vorgehensweise vermeiden. Wenn eine Eintrags-ID wieder verwendet werden muss, sollten Dienstanbieter den Zeitraum zwischen der anfänglichen Verwendung und der Wiederverwendung so lange wie möglich verstreichen lassen. Außerdem sollte die Eintrags-ID einem anderen Objekt desselben Typs erneut zugewiesen werden. Das heißt, eine bestimmte Eintrags-ID sollte nicht zuerst einer Nachricht und dann mit einem Ordner zugeordnet werden.
  
## <a name="see-also"></a>Siehe auch



[MAPI-Eintrags-IDs](mapi-entry-identifiers.md)

