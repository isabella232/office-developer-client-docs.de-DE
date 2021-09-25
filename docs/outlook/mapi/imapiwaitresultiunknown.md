---
title: 'IMAPIWaitResult : IUnknown'
manager: lindalu
ms.date: 04/27/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIWAITRESULT
api_type:
- COM
ms.assetid: d7157f57-709d-4e53-973b-176954e2bb73
description: IMAPIWaitResult
Last modified: April 27, 2021
ms.openlocfilehash: 624c9e60e2ca12f280c4f754986a10aee7735b10
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584346"
---
# <a name="imapiwaitresult--iunknown"></a>IMAPIWaitResult : IUnknown
  
**Gilt für**: Outlook 2013 | Outlook 2016 | Outlook 2019

Diese Schnittstelle wird von Consumern von IMAPIInitMonitor verwendet, um zu steuern, wo die Wartezeit erfolgt. Sie können das Objekt in einem Thread erstellen und in einen anderen Thread verschieben, um die tatsächliche Wartezeit auszuführen.

## <a name="vtable-order"></a>VTable-Reihenfolge

| Funktion | description |
|:-----|:-----|
|[HRESULT IMAPIWaitResult::End()](imapiwaitresult-end.md)|Wird aufgerufen, um die Blockierung in dem Thread zu initiieren, in dem sie aufgerufen wird. Dabei muss es sich nicht um den thread, der *IMAPIInitMonitor::BeginWait* aufgerufen hat, sein.|

| Quickinfos | result |
|:-----|:-----|
|Erbt von:  <br/> |IUnknown  <br/> |
|Implementiert von:  <br/> |  OLMAPI32.DLL<br/> |
|Aufgerufen von:  <br/> |Clientanwendungen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIWaitResult  <br/> |

## <a name="see-also"></a>Siehe auch

[IMAPIInitMonitor](imapiinitmonitoriunknown.md)

[IMAPIInitMonitor::BeginWait](imapiinitmonitor-beginwait.md)

[IMAPIInitMonitor : IUnknown](imapiinitmonitoriunknown.md)

[CreateMAPIInitializationMonitor](createmapiinitializationmonitor.md)
