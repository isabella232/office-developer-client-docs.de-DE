---
title: Fehlerbehandlung in MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 99e2c485-af84-46f4-84b4-fca2117b5a21
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7186964768f182416d718d42f62f8ee1ce048a3c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614255"
---
# <a name="error-handling-in-mapi"></a>Fehlerbehandlung in MAPI

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erfolgs-, Warnungs- und Fehlerwerte werden mithilfe einer 32-Bit-Nummer zurückgegeben, die als Ergebnishandle oder HRESULT bezeichnet wird. Ein HRESULT ist eigentlich kein Handle für etwas; Es handelt sich lediglich um einen 32-Bit-Wert mit mehreren im Wert codierten Feldern. Ein Nullergebnis bedeutet Erfolg und ein Ergebnis ungleich Null gibt einen Fehler an.
  
MAPI auf 32-Bit-Plattformen funktioniert ausschließlich mit HRESULT-Werten.
  
Die folgende Abbildung zeigt das HRESULT-Format für 32-Bit-Plattformen.
  
**HRESULT-Format**
  
![HRESULT-Format](media/amapi_49.gif "HRESULT-Format")
  
Das Bit in hoher Reihenfolge im HRESULT gibt an, ob der Rückgabewert erfolg- oder fehleraufwendig ist. Wenn dieser Wert auf Null festgelegt ist, gibt der Wert den Erfolg an. Wenn der Wert auf 1 festgelegt ist, wird ein Fehler angezeigt.
  
Die Bits R, C, N und r sind im HRESULT reserviert.
  
Das Einrichtungsfeld in beiden Versionen gibt den Zuständigkeitsbereich für den Fehler an. Es gibt mehrere Möglichkeiten, aber der Großteil der MAPI-Fehler verwendet FACILITY_ITF, um Schnittstellenfehler darzustellen. Die am häufigsten verwendeten Einrichtungen sind: FACILITY_NULL, FACILITY_ITF, FACILITY_DISPATCH, FACILITY_RPC und FACILITY_STORAGE. Wenn neue Einrichtungen erforderlich sind, weist Microsoft sie zu, da sie eindeutig sein müssen. In der folgenden Tabelle werden die verschiedenen Einrichtungsfelder beschrieben.
  
|Facility|Beschreibung|
|:-----|:-----|
|FACILITY_NULL  <br/> |Für allgemein anwendbare allgemeine Statuscodes wie S_OK oder E_OUTOF_MEMORY; der Wert ist Null.  <br/> |
|FACILITY_ITF  <br/> |Für die meisten Statuscodes, die von Schnittstellenmethoden zurückgegeben werden; der Wert wird von der Schnittstelle definiert. Das heißt, zwei HRESULT-Werte mit genau dem gleichen 32-Bit-Wert, der von zwei verschiedenen Schnittstellen zurückgegeben wird, können unterschiedliche Bedeutungen haben.  <br/> |
|FACILITY_DISPATCH  <br/> |Bei Fehlern bei der [IDispatch-Schnittstelle](https://msdn.microsoft.com/library/ms221608.aspx) für spätes Binden.  <br/> |
|FACILITY_RPC  <br/> |Für Statuscodes, die von Remoteprozeduraufrufen zurückgegeben werden.  <br/> |
|FACILITY_STORAGE  <br/> |Für Statuscodes, die von [IStorage-](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) oder [IStream-Methodenaufrufen](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) im Zusammenhang mit strukturiertem Speicher zurückgegeben werden. Statuscodes mit Codewerten (untere 16 Bits) im Bereich Windows Fehlercodes (d. h. kleiner als 256) haben die gleiche Bedeutung wie die entsprechenden Windows Fehler.  <br/> |
   
Das Codefeld ist eine eindeutige Zahl, die zur Darstellung des Fehlers oder der Warnung zugewiesen ist.
  

