---
title: Erstellen von Eintragsbezeichnern
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: bc2a9116-948e-4da3-96b8-26d73bcd63c4
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a68ac05659d6116bb40ea136aa40b49110d4226a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611023"
---
# <a name="constructing-entry-identifiers"></a>Erstellen von Eintragsbezeichnern

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eintragsbezeichner werden mit der [ENTRYID-Struktur](entryid.md) erstellt. Die **ENTRYID-Struktur** besteht aus einem Flag, das die Attribute des Eintragsbezeichners und des tatsächlichen Eintragsbezeichners beschreibt. 
  
## <a name="entryid-structure"></a>ENTRYID-Struktur

Die **ENTRYID-Struktur** ist wie folgt definiert: 
  
```cpp
typedef struct
{
    BYTE        abFlags[4];
    BYTE        ab[MAPI_DIM];
}  ENTRYID, FAR *LPENTRYID;
 
```

MAPI_DIM ist eine Konstante, die in der Headerdatei MapiDefs.h definiert ist. 
  
Das erste Byte des 4-Byte-Elements **abFlags** beschreibt den Typ und die Verwendung des Eintragsbezeichners und kann die folgenden Werte aufweisen: 
  
- MAPI_NOTRECI - Gibt an, dass der Eintragsbezeichner nicht als Empfänger einer Nachricht verwendet werden kann.
    
- MAPI_NOTRESERVED - Gibt an, dass andere Benutzer nicht auf den Eintragsbezeichner zugreifen können.
    
- MAPI_NOW - Gibt an, dass der Eintragsbezeichner nicht zu anderen Zeiten verwendet werden kann.
    
- MAPI_SHORTTERM - Gibt an, dass der Eintragsbezeichner kurzfristig ist. Alle anderen Werte in diesem Byte müssen festgelegt werden, es sei denn, andere Verwendungen des Eintragsbezeichners sind zulässig.
    
- MAPI_THISSESSION - Gibt an, dass der Eintragsbezeichner nicht in anderen Sitzungen verwendet werden kann.
    
- MAPI_NOTRESERVED - Gibt an, dass der Eintragsbezeichner von anderen Dienstanbietern für andere Objekte verwendet werden kann.
    
Das **Element** von Eintragsbezeichnern, die von Adressbuch- und Nachrichtenspeicheranbietern erstellt werden, besteht aus zwei Teilen: einer [MAPIUID-Struktur](mapiuid.md) mit 16 Byte, die den Dienstanbieter identifiziert, und einem Teil zum Identifizieren des Objekts. **MAPIUID** ist eine Struktur, die einen global eindeutigen Bezeichner oder eine GUID enthält. Eine GUID ist ein bytereihenfolgeunabhängiger Bezeichner, der mithilfe des Tools Microsoft Visual Studio *GUID** erstellt werden kann. 
  
Ein Dienstanbieter registriert seine **MAPIUID-Struktur** bei der MAPI während des Anmeldevorgangs in einem Aufruf der [IMAPISupport::SetProviderUID-Methode.](imapisupport-setprovideruid.md) Wenn ein Client eine **OpenEntry-Methode** aufruft, um auf ein Objekt zuzugreifen, verwendet MAPI die **MAPIUID-Struktur,** um zu bestimmen, welcher Dienstanbieter diesen Zugriff bereitstellen kann. Dienstanbieter sollten dieselbe **MAPIUID-Struktur** für alle Versionen ihrer DLL verwenden. Dadurch können Clients mit der neueren Version auf Nachrichten reagieren, die mit der älteren Version gesendet und gespeichert wurden. 
  
Der Rest des **Ab-Elements** nach dem 16-Byte-MAPIUID enthält dienstanbieterspezifische Binärdaten zum Identifizieren bestimmter Objekte.  Für diesen Teil des Eintragsbezeichners gibt es keine feste Größe. Es kann eine beliebige Größe innerhalb des Grunds sein. Ein Dienstanbieter enthält in der Regel die folgenden Informationen in diesem Teil seiner Eintragsbezeichner: 
  
- Versionsinformationen – Da es üblich ist, dass ein Dienstanbieter das Format seiner Eintragsbezeichner von Version zu Version ändert, können durch das Speichern von Versionsinformationen schnell ermittelt werden, wie ein Eintragsbezeichner entschlüsselt werden soll.
    
- Standortinformationen – Standortinformationen sind Daten, die einem Dienstanbieter einen Indikator dafür bieten, wie das durch den Eintragsbezeichner dargestellte Objekt gefunden wird. Beispielsweise kann ein Dienstanbieter den Datenträgeroffset für die letzte Stelle in einer Datendatei speichern, in der das Objekt gespeichert wurde. Da sich diese Art von Informationen im Laufe der Zeit ändern kann, sollten Dienstanbieter mehrere Möglichkeiten zum Suchen von Objekten in ihren Eintragsbezeichnern bereitstellen.
    
Obwohl Dienstanbieter ihre Eintrags-IDs wiederverwenden können, sollten sie diese Vorgehensweise vermeiden. Wenn es erforderlich ist, einen Eintragsbezeichner wiederzuverwenden, sollten Dienstanbieter den Zeitraum, der zwischen der ursprünglichen Verwendung und der Wiederverwendung verstrichen ist, so lange wie möglich festlegen. Außerdem sollte der Eintragsbezeichner einem anderen Objekt desselben Typs neu zugewiesen werden. Das heißt, ein bestimmter Eintragsbezeichner sollte nicht zuerst einer Nachricht und dann einem Ordner zugeordnet werden.
  
## <a name="see-also"></a>Siehe auch



[MAPI-Eintragsbezeichner](mapi-entry-identifiers.md)

