---
title: Fehlerbehandlung in MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99e2c485-af84-46f4-84b4-fca2117b5a21
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 98ee0856411cce3a3e9012185be6c30503de7779
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287280"
---
# <a name="error-handling-in-mapi"></a>Fehlerbehandlung in MAPI

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erfolgs-, Warnungs- und Fehlerwerte werden mithilfe einer 32-Bit-Nummer zurückgegeben, die als Ergebnishandle oder HRESULT bezeichnet wird. Ein HRESULT ist wirklich kein Handle für etwas; Es handelt sich lediglich um einen 32-Bit-Wert mit mehreren Feldern, die im Wert codiert sind. Ein Nullergebnis gibt den Erfolg an, und ein Ergebnis ungleich Null gibt einen Fehler an.
  
MAPI auf 32-Bit-Plattformen funktioniert ausschließlich mit HRESULT-Werten.
  
Die folgende Abbildung zeigt das HRESULT-Format für 32-Bit-Plattformen.
  
**HRESULT-Format**
  
![HRESULT-Format](media/amapi_49.gif "HRESULT-Format")
  
Das Bit mit hoher Reihenfolge im HRESULT gibt an, ob der Rückgabewert Erfolg oder Fehler darstellt. Wenn dieser Wert auf Null festgelegt ist, gibt der Wert den Erfolg an. Wenn dieser Wert auf 1 festgelegt ist, wird ein Fehler angezeigt.
  
Die Bits R, C, N und r sind im HRESULT reserviert.
  
Das Feld Einrichtung in beiden Versionen gibt den Verantwortungsbereich für den Fehler an. Es gibt mehrere Möglichkeiten, aber die überwiegende Mehrzahl der MAPI-Fehler FACILITY_ITF zur Darstellung von Schnittstellenfehlern. Die gängigsten Derzeit verwendeten Einrichtungen sind: FACILITY_NULL, FACILITY_ITF, FACILITY_DISPATCH, FACILITY_RPC und FACILITY_STORAGE. Wenn neue Einrichtungen erforderlich sind, ordnet Microsoft sie zu, da sie eindeutig sein müssen. In der folgenden Tabelle werden die verschiedenen Einrichtungsfelder beschrieben.
  
|Facility|Beschreibung|
|:-----|:-----|
|FACILITY_NULL  <br/> |Für allgemein anwendbare allgemeine Statuscodes wie S_OK oder E_OUTOF_MEMORY; der Wert ist Null.  <br/> |
|FACILITY_ITF  <br/> |Für die meisten von Schnittstellenmethoden zurückgegebenen Statuscodes; der Wert wird durch die Schnittstelle definiert. Das heißt, zwei HRESULT-Werte mit exakt demselben 32-Bit-Wert, der von zwei verschiedenen Schnittstellen zurückgegeben wird, können unterschiedliche Bedeutungen haben.  <br/> |
|FACILITY_DISPATCH  <br/> |Bei Fehlern bei der [späten Bindung der IDispatch-Schnittstelle.](https://msdn.microsoft.com/library/ms221608.aspx)  <br/> |
|FACILITY_RPC  <br/> |Für Statuscodes, die von Remoteprozeduraufrufen zurückgegeben werden.  <br/> |
|FACILITY_STORAGE  <br/> |Für Statuscodes, die von [IStorage-](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) oder [IStream-Methodenaufrufen im](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) Zusammenhang mit strukturiertem Speicher zurückgegeben werden. Statuscodes mit Codewerten (unter 16 Bit) im Bereich von Windows-Fehlercodes (d. h. weniger als 256) haben dieselbe Bedeutung wie die entsprechenden Windows-Fehler.  <br/> |
   
Das Codefeld ist eine eindeutige Zahl, die zur Darstellung des Fehlers oder der Warnung zugewiesen ist.
  

