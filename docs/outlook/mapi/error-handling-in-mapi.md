---
title: Fehlerbehandlung in MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99e2c485-af84-46f4-84b4-fca2117b5a21
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 98ee0856411cce3a3e9012185be6c30503de7779
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287280"
---
# <a name="error-handling-in-mapi"></a>Fehlerbehandlung in MAPI

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erfolgs-, Warnungs-und Fehlerwerte werden mit einer 32-Bit-Zahl zurückgegeben, die als Ergebnis-Handle oder HRESULT bezeichnet wird. Ein HRESULT ist wirklich kein Handle für alles; Es handelt sich lediglich um einen 32-Bit-Wert mit mehreren Feldern, die im Wert codiert sind. Ein Ergebnis von NULL gibt den Erfolg an, und ein Ergebnis ungleich NULL weist auf einen Fehler hin.
  
MAPI auf 32-Bit-Plattformen funktioniert ausschließlich mit HRESULT-Werten.
  
Die folgende Abbildung zeigt das HRESULT-Format für 32-Bit-Plattformen.
  
**HRESULT-Format**
  
![HRESULT-Format] (media/amapi_49.gif "HRESULT-Format")
  
Das hochwertige Bit im HRESULT gibt an, ob der Rückgabewert Erfolg oder Misserfolg darstellt. Bei Festlegung auf 0 (null) gibt der Wert Erfolg an. Bei Festlegung auf 1 wird ein Fehlschlagen angezeigt.
  
Die Bits R, C, N und r sind im HRESULT reserviert.
  
Das Feld "Anlage" in beiden Versionen gibt den Zuständigkeitsbereich für den Fehler an. Es gibt mehrere Möglichkeiten, aber die meisten MAPI-Fehler verwenden FACILITY_ITF, um Schnittstellenfehler darzustellen. Die am häufigsten verwendeten Einrichtungen sind: FACILITY_NULL, FACILITY_ITF, FACILITY_DISPATCH, FACILITY_RPC und FACILITY_STORAGE. Wenn neue Einrichtungen erforderlich sind, weist Microsoft Sie an, da Sie eindeutig sein müssen. In der folgenden Tabelle werden die verschiedenen Facility-Felder beschrieben.
  
|Facility|Beschreibung|
|:-----|:-----|
|FACILITY_NULL  <br/> |Für allgemein gültige allgemeine Statuscodes wie S_OK oder E_OUTOF_MEMORY; der Wert ist NULL.  <br/> |
|FACILITY_ITF  <br/> |Für die meisten von Schnittstellenmethoden zurückgegebenen Statuscodes; der Wert wird von der Schnittstelle definiert. Das heißt, zwei HRESULT-Werte mit genau demselben 32-Bit-Wert, die von zwei verschiedenen Schnittstellen zurückgegeben werden, haben möglicherweise unterschiedliche Bedeutungen.  <br/> |
|FACILITY_DISPATCH  <br/> |Bei spätem Binden von [IDispatch](https://msdn.microsoft.com/library/ms221608.aspx) -Schnittstellenfehlern.  <br/> |
|FACILITY_RPC  <br/> |Für Statuscodes, die von Remoteprozeduraufrufen zurückgegeben werden.  <br/> |
|FACILITY_STORAGE  <br/> |Für Statuscodes, die von [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) -oder [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) -Methoden aufrufen im Zusammenhang mit strukturiertem Speicher zurückgegeben werden. Status Codes mit Code (niedrigeren 16-Bit-Werten) im Windows-Fehlercode (also weniger als 256) haben dieselbe Bedeutung wie die entsprechenden Windows-Fehler.  <br/> |
   
Das Feld Code ist eine eindeutige Nummer, die dem Fehler oder der Warnung zugeordnet ist.
  

