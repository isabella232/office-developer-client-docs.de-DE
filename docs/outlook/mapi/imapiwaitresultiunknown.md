---
title: 'IMAPIWaitResult : IUnknown'
manager: lindalu
ms.date: 04/26/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIWAITRESULT
api_type:
- COM
ms.assetid: d7157f57-709d-4e53-973b-176954e2bb73
description: IMAPIWaitResult
Last modified: April 26, 2021
ms.openlocfilehash: 67a0fffdd0ab6d4989c12568f4d89808ba5adc7a
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062039"
---
# <a name="imapiwaitresult--iunknown"></a>IMAPIWaitResult : IUnknown
  
**Gilt für**: Outlook 2013 | Outlook 2016 | Outlook 2019

Diese Schnittstelle wird von Verbrauchern von IMAPIInitMonitor verwendet, um zu steuern, wo das Warten erfolgt. Es ermöglicht ihnen, das Objekt in einem Thread zu erstellen und es in einen anderen Thread zu verschieben, um das tatsächliche Warten durchzuführen.

## <a name="vtable-order"></a>Vtable-Reihenfolge

| Funktion | description |
|:-----|:-----|
|[HRESULT IMAPIWaitResult::End()](imapiwaitresult-end.md)|Wird aufgerufen, um das Blockieren des Threads zu initiieren, in dem er aufgerufen wird. Dabei muss es sich nicht um denselben Thread wie *IMAPIInitMonitor::BeginWait handelt.*|

| Schnellinfos | result |
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
