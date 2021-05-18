---
title: Fenster-Schnittstellen (OneNote 2013)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e6900ad7-c147-4816-93a9-5773170b115a
description: Die Schnittstellen Window und Windows sind OneNote 2013-API-Objekte, die Benutzern die Arbeit mit OneNote-Fenster ermöglicht. Diese Objekte ermöglichen Benutzern bestimmte Fenstereigenschaften zu durchlaufen, den Satz von OneNote-Fenster.
ms.openlocfilehash: efc34312def588ecff54c63b3db84f8bf909352b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317035"
---
# <a name="window-interfaces-onenote"></a>Fenster-Schnittstellen (OneNote 2013)

Die Schnittstellen **Window** und **Windows** sind OneNote 2013-API-Objekte, die Benutzern die Arbeit mit OneNote-Fenster ermöglicht. Diese Objekte ermöglichen Benutzern bestimmte Fenstereigenschaften zu durchlaufen, den Satz von OneNote-Fenster. 
  
## <a name="onenote-window-views"></a>OneNote-Fensteransichten

Die folgende Liste enthält die vier Ansichtsmodi, die Sie für OneNote-Fenster verwenden können: 
  
- Normalansicht - zeigt das standardmäßige OneNote-Fenster in der Navigationsbereiche Notizbuch und Seite sichtbar sind.
    
- Vollständiger Seitenansicht - Zeigt eine minimale Benutzeroberfläche (UI) anzeigen, in dem die Panes-Notizbuch und die Seite nicht angezeigt werden.
    
- Kurznotiz - zeigt ein kleines Fenster, das Benutzern erlaubt, kurze Notizen machen. Sie würden in der Regel Kurznotizen zugreifen, über das OneNote-Symbol im Windows-Infobereich, aber Sie können sie auch zugreifen, über die Registerkarte **Ansicht** in OneNote. 
    
- Andocken auf Desktop - ein OneNote-Fenster, das Sie andocken können auf jeder Seite des Desktops (vergleichbar mit der Taskleiste) angezeigt. Diese Ansicht reduziert die Größe des Desktops, um das Fenster passt. Sie können nur ein Fenster andocken, können Sie jederzeit und das Fenster ist immer sichtbar, ohne den Desktop blockieren. 
    
Die folgende Abbildung zeigt, wie die Vollseitenansicht, die Dock-to-Desktop-Ansicht und schnelle Notizen auf Ihrem Desktop aussehen.
  
**OneNote-Ansichten**

![OneNote Fensteransichten OneNote](media/ON15Con_views.jpg "Fensteransichten")
  
## <a name="interfaces"></a>Schnittstellen

In diesem Abschnitt werden die Schnittstellen und Member, die Sie zum programmgesteuerten Ändern der OneNote-Fenster verwenden können.
  
### <a name="windows-interface"></a>Windows-Schnittstelle

Die **Windows** -Schnittstelle ermöglicht es dem Benutzer, die den Satz von geöffnete OneNote-Fenster zuzugreifen. Es ist eine Eigenschaft der OneNote- **Application** -Klasse über **Application.Windows** zugegriffen. Dies gibt den aufgelisteten Satz von OneNote-Fenster zurück. 
  
**Eigenschaften**

|**Name**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|**Count** <br/> |ulong  <br/> |Ruft die Anzahl der **Window** -Objekte in der Gruppe **Windows**.  <br/> |
|**CurrentWindow** <br/> |**Window** <br/> |Ruft das **Window** -Objekt des aktiven Fensters OneNote.  <br/> |
|**Items** <br/> |**Window** <br/> |Gibt das Objekt **Window**, das entspricht dem Index-Wert übergeben. Diese Eigenschaft kann nicht direkt zugegriffen werden. Verwenden Sie **Windows [(uint) index]**, um ein **Window** -Objekt zurückzugeben.  <br/> |
   
### <a name="window-interface"></a>Fensterschnittstelle

Die **Window** -Schnittstelle ermöglicht es dem Benutzer Zugriff auf bestimmte Eigenschaften der einzelnen Fenster. Jedes Fenster OneNote kann durch Auflisten der **Windows** -Eigenschaft der **Application** -Klasse zugegriffen werden. 
  
**Eigenschaften**

|**Name**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|**Active** <br/> |bool  <br/> |Dient zum Abrufen oder Festlegen eines Werts, das angibt, ob das Fenster das aktive Fenster OneNote.  <br/> |
|**Anwendung** <br/> |**Anwendung** <br/> |Ruft das OneNote **Application** -Objekt, das dem Fenster zugeordnet ist.  <br/> |
|**CurrentPageId** <br/> |string  <br/> |Ruft die Objekt-ID der aktiven OneNote-Seite des Fensters ab.  <br/> |
|**CurrentSectionId** <br/> |string  <br/> |Ruft die Objekt-ID des aktiven OneNote-Abschnitt des Fensters ab.  <br/> |
|**CurrentSectionGroupId** <br/> |string  <br/> |Ruft die Objekt-ID der aktiven OneNote im Abschnittsgruppe des Fensters ab.  <br/> |
|**CurrentNotebookId** <br/> |string  <br/> |Ruft die Objekt-ID der aktiven OneNote-Notizbuch des Fensters ab.  <br/> |
|**DockedLocation** <br/> |**DockedLocation** <br/> |Dient zum Abrufen oder Festlegen des angedockten Speicherorts des OneNote-Fensters.  <br/> |
|**FullPageView** <br/> |bool  <br/> |Dient zum Abrufen oder Festlegen eines Werts, das angibt, ob das Fenster Ganzseitenansicht (minimaler Benutzeroberfläche anzeigen).  <br/> |
|**SideNote** <br/> |bool  <br/> |Dient zum Abrufen oder Festlegen eines Werts, das angibt, ob das Fenster ein Kurznotiz Fenster ist.  <br/> |
|**WindowHandle** <br/> |ulong  <br/> |Ruft die ID Handle des OneNote-Fensters.  <br/> |
   
**Methoden**
  
Die folgenden Methoden der **Window** -Schnittstelle können Sie angegebenen Objekten in OneNote-Fensters oder zum angegebenen URLs navigieren. 
  
**NavigateTo**

|||
|:-----|:-----|
|**Beschreibung** <br/> |Navigiert zu dem angegebenen Objekt in der OneNote-Fenster. Beispielsweise können Sie die Abschnitte, Seiten und Gliederung Schemaelemente in Seiten navigieren.  <br/> |
|**Syntax** <br/> | `HRESULT NavigateTo(`           ` [in]BSTR bstrHierarchyObjectID, `           ` [in]BSTR bstrObjectID); ` <br/> |
|**Parameter** <br/> | _bstrHierarchyObjectID_- der Hierarchie OneNote-ID des Objekts, zu dem navigiert werden soll. Die Objekt-ID kann eine OneNote-Notizbuch, Abschnitt, Abschnittsgruppe oder Seite verweisen. <br/>  _bstrObjectID_- die OneNote-ID des Objekts innerhalb einer OneNote-Seite zu navigieren. Dieser Parameter wird festgelegt, wenn der Benutzer nicht auf ein bestimmtes Objekt auf einer Seite navigieren möchten, auf Null. <br/> |
   
**NavigateToUrl**

|||
|:-----|:-----|
|**Beschreibung** <br/> |Wenn einen Link OneNote übergeben (Onenote: / /), wird das OneNote-Fenster auf den entsprechenden Speicherort in OneNote geöffnet. Wenn es sich bei dem Link jedoch um einen externen Link handelt, z. B. https:// oder file://, wird ein Sicherheitsdialogfeld angezeigt. Bei Kündigung OneNote versucht, um den Link zu öffnen, und ein HResult.hrObjectDoesNotExist-Fehler zurückgegeben.  <br/> |
|**Syntax** <br/> | `HRESULT NavigateToUrl (`           ` [in]BSTR bstrUrl); ` <br/> |
|**Parameter** <br/> | _bstrUrl_- die URL zu navigieren.  <br/> |
   
**SetDockedLocation**

|||
|:-----|:-----|
|**Beschreibung** <br/> |Das Fenster von **dockLocation** und den Monitor am **ptMonitor** angegebene Position angedockt.  <br/> |
|**Syntax** <br/> | `HRESULT SetDockedLocation`(           `[in] DockLocation dockLocation,`           `[in] POINT ptMonitor);` <br/> |
|**Parameter** <br/> | _dockLocation_ - gibt die angedockte Position eines Fensters OneNote 2013.  <br/>  _ptMonitor_ - (Optional) gibt an, dass in x-und y-Koordinaten, die das Fenster Überwachen verankert werden sollte.  <br/> |
   
## <a name="example"></a>Beispiel

Der folgende Code durchläuft die OneNote-Fenster, ein angedocktes Fenster zu erhalten. Wenn kein angedocktes Fenster vorhanden ist, wird im Beispiel wird das aktive Fenster angedockt. Wenn kein aktives Fenster vorhanden ist, erstellt der Code ein neues angedocktes Fenster.
  
```cs
using System;
using System.Diagnostics;
using Microsoft.Office.Interop.OneNote;
namespace SampleWND
{
    class DockOneNoteWindow
    {
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = new Microsoft.Office.Interop.OneNote.Application();
            // Search through all OneNote windows for a docked window and activate it.
            bool foundDockedWND = false;
            for (int i = 0; i < app.Windows.Count; i++)
            {
                if (app.Windows[(uint) i].DockedLocation != DockLocation.dlNone)
                {
                    foundDockedWND = true;
                    app.Windows[(uint) i].Active = true;
                }
            }
            
            // If no docked window exists, dock the active window.
            if (!foundDockedWND && (app.Windows.Count > 0))
                app.Windows.CurrentWindow.DockedLocation = DockLocation.dlDefault;
            // If no active window exists, create a new docked window.
            if (app.Windows.Count < 1)
            {
                Process oneProc = new Process();
                oneProc.StartInfo.FileName = "onenote.exe";
                oneProc.StartInfo.Arguments = "/docked";
                oneProc.Start();
            }
        }
    }
}

```

## <a name="see-also"></a>Siehe auch

- [OneNote-Entwicklerreferenz](onenote-developer-reference.md)

