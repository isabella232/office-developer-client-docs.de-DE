---
title: Erstellen von Eintragsbezeichnern
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bc2a9116-948e-4da3-96b8-26d73bcd63c4
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8d48c2584fa5b7e862102e401ea8165821607f77
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427948"
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

MAPI_DIM ist eine Konstante, die in der MapiDefs.h-Headerdatei definiert ist. 
  
Das erste Byte des 4-Byte-AbFlags-Mitglieds beschreibt den Typ und die Verwendung der Eintrags-ID und kann die folgenden Werte haben:  
  
- MAPI_NOTRECI – Gibt an, dass der Eintragsbezeichner nicht als Empfänger für eine Nachricht verwendet werden kann.
    
- MAPI_NOTRESERVED – Gibt an, dass andere Benutzer nicht auf die Eintrags-ID zugreifen können.
    
- MAPI_NOW – Gibt an, dass der Eintragsbezeichner zu anderen Zeiten nicht verwendet werden kann.
    
- MAPI_SHORTTERM – Gibt an, dass der Eintragsbezeichner kurzfristig ist. Alle anderen Werte in diesem Byte müssen festgelegt werden, es sei denn, andere Verwendungen der Eintrags-ID sind zulässig.
    
- MAPI_THISSESSION – Gibt an, dass der Eintragsbezeichner nicht für andere Sitzungen verwendet werden kann.
    
- MAPI_NOTRESERVED – Gibt an, dass der Eintragsbezeichner von anderen Dienstanbietern für andere Objekte verwendet werden kann.
    
Das **ab-Element** von Eintragsbezeichnern, die von Adressbuch- und Nachrichtenspeicheranbietern erstellt werden, besteht aus zwei Teilen: einer [MAPIUID-Struktur](mapiuid.md) mit 16 Byte, die den Dienstanbieter identifiziert, und einem Element zum Identifizieren des Objekts. **MAPIUID** ist eine Struktur, die einen global eindeutigen Bezeichner oder eine GUID enthält. Eine GUID ist ein bytereihenfolgeunabhängiger Bezeichner, der mithilfe des Tools Microsoft Visual Studio *GUID** erstellen erstellt werden kann. 
  
Ein Dienstanbieter registriert seine **MAPIUID-Struktur** bei MAPI während des Anmeldevorgangs in einem Aufruf der [IMAPISupport::SetProviderUID-Methode.](imapisupport-setprovideruid.md) Wenn ein Client eine **OpenEntry-Methode** aufruft, um auf ein Objekt zu zugreifen, verwendet MAPI die **MAPIUID-Struktur,** um zu bestimmen, welcher Dienstanbieter diesen Zugriff bereitstellen kann. Dienstanbieter sollten dieselbe **MAPIUID-Struktur** für alle Versionen ihrer DLL verwenden. Dadurch können Clients mit der neueren Version auf Nachrichten reagieren, die mit der älteren Version gesendet und gespeichert wurden. 
  
Der Rest des **ab-Mitglieds** nach dem 16-Byte-MAPIUID enthält dienstanbieterspezifische Binärdaten zum Identifizieren bestimmter Objekte.  Für diesen Teil der Eintrags-ID gibt es keine feste Größe. Es kann eine beliebige Größe sein, innerhalb der Grund. Ein Dienstanbieter enthält in der Regel die folgenden Informationen in diesem Teil seiner Eintragsbezeichner: 
  
- Versionsinformationen – Da es für einen Dienstanbieter üblich ist, das Format seiner Eintragsbezeichner von Version zu Version zu ändern, können Durch das Speichern von Versionsinformationen schnell bestimmt werden, wie jeder Eintragsbezeichner entschlüsselt werden kann.
    
- Standortinformationen – Standortinformationen sind Daten, die einem Dienstanbieter einen Indikator dafür geben, wie das durch den Eintragsbezeichner dargestellte Objekt gefunden wird. Beispielsweise kann ein Dienstanbieter den Datenträgerversatz für den letzten Ort in einer Datendatei speichern, in der das Objekt gespeichert wurde. Da sich diese Art von Informationen im Laufe der Zeit ändern kann, sollten Dienstanbieter mehrere Möglichkeiten zum Auffinden von Objekten in ihren Eintragsbezeichnern bereitstellen.
    
Obwohl Dienstanbieter ihre Eintrags-ID wiederverwenden können, sollten sie diese Vorgehensweise vermeiden. Wenn eine Eintrags-ID wiederverwendet werden muss, sollten Dienstanbieter den Zeitraum zwischen der anfänglichen Verwendung und der Wiederverwendung so lange wie möglich angeben. Außerdem sollte der Eintragsbezeichner einem anderen Objekt desselben Typs neu zugewiesen werden. Das heißt, eine bestimmte Eintrags-ID sollte nicht zuerst einer Nachricht und dann einem Ordner zugeordnet werden.
  
## <a name="see-also"></a>Siehe auch



[MAPI-Eintragsbezeichner](mapi-entry-identifiers.md)

