---
title: Multithreading und Memory Contention in Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- Multithreading in Excel, Arbeitsspeicher-Streit in Excel,Funktionen [Excel 2007], threadsichere, threadsichere Funktionen [Excel 2007],thread-lokaler Speicher [Excel 2007]
localization_priority: Normal
ms.assetid: 86e1e842-f433-4ea9-8b13-ad2515fc50d8
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a385728450fc6519d7f5211c186a9d74e623bf7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301638"
---
# <a name="multithreading-and-memory-contention-in-excel"></a>Multithreading und Memory Contention in Excel

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Versionen von Microsoft Excel vor Excel 2007 verwenden einen einzelnen Thread für alle Arbeitsblattberechnungen. Ab Excel 2007 kann Excel für die Verwendung von 1 bis 1024 gleichzeitigen Threads für die Arbeitsblattberechnung konfiguriert werden. Auf einem Computer mit mehreren Prozessoren oder mehreren Kernen entspricht die Standardanzahl von Threads der Anzahl der Prozessoren oder Kerne. Daher können threadsichere Zellen oder Zellen, die nur threadsichere Funktionen enthalten, gleichzeitigen Threads zugewiesen werden, vorbehaltlich der üblichen Neuberechnungslogik, die nach ihren Vorgängern berechnet werden muss.
  
## <a name="thread-safe-functions"></a>Thread-Safe-Funktionen

Die meisten integrierten Arbeitsblattfunktionen ab Excel 2007 sind threadsicher. Sie können auch XLL-Funktionen als threadsicher schreiben und registrieren. Excel verwendet einen Thread (seinen Hauptthread), um alle Befehle, threadunsicheren Funktionen, **xlAuto-Funktionen** (außer [xlAutoFree](xlautofree-xlautofree12.md) und **xlAutoFree12)** und COM- und Visual Basic for Applications (VBA)-Funktionen auf aufruft.
  
Wenn eine XLL-Funktion einen **XLOPER-** oder **XLOPER12-Wert** mit **xlbitDLLFree-Satz** zurückgibt, verwendet Excel denselben Thread, für den der Funktionsaufruf zum Aufrufen von **xlAutoFree** oder **xlAutoFree12** ausgeführt wurde. Der Aufruf von **xlAutoFree** oder **xlAutoFree12** erfolgt vor dem nächsten Funktionsaufruf in diesem Thread. 
  
Für XLL-Entwickler gibt es Vorteile für das Erstellen threadsicherer Funktionen:
  
- Sie ermöglichen Excel, das Beste aus einem Multiprozessor- oder Multi-Core-Computer zu machen.
    
- Sie eröffnen die Möglichkeit, Remoteserver viel effizienter zu verwenden, als dies mit einem einzigen Thread möglich ist.
    
Angenommen, Sie verfügen über einen Computer mit einem Prozessor, der für die Verwendung, z. B.  *N-Threads, konfiguriert*  wurde. Angenommen, es wird eine Kalkulationstabelle ausgeführt, die eine große Anzahl von Aufrufen an eine XLL-Funktion sendet, die wiederum eine Anforderung für Daten oder eine Berechnung an einen Remoteserver oder Cluster von Servern sendet. Abhängig von der Topologie der Abhängigkeitsstruktur Excel die Funktion fast zeitgleich aufrufen. Vorausgesetzt, der Server oder die Server sind ausreichend schnell oder parallel, kann die Neuberechnungszeit der Tabelle um den Faktor 1/N reduziert werden. 
  
Das wichtigste Problem beim Schreiben von threadsicheren Funktionen ist die korrekte Behandlung von Ressourceninhalten. Dies bedeutet in der Regel Speicher-Streit, und er kann in zwei Probleme aufgeschlüsselt werden:
  
- So erstellen Sie Speicher, von dem Sie wissen, dass er nur von diesem Thread verwendet wird.
    
- So stellen Sie sicher, dass auf freigegebenen Arbeitsspeicher von mehreren Threads sicher zugegriffen wird.
    
Zunächst ist zu beachten, auf welchen Speicher in einer XLL alle Threads und nur der aktuell ausgeführte Thread zugriffen kann.
  
 **Zugriff durch alle Threads**
  
- Variablen, Strukturen und Klasseninstanzen, die außerhalb des Textkörpers einer Funktion deklariert werden.
    
- Statische Variablen, die innerhalb des Textkörpers einer Funktion deklariert werden.
    
In diesen beiden Fällen wird der Arbeitsspeicher im Speicherblock der DLL, der für diese Instanz der DLL erstellt wurde, beiseite gelegt. Wenn eine andere Anwendungsinstanz die DLL lädt, ruft sie eine eigene Kopie dieses Speichers ab, sodass es keinen Streit über diese Ressourcen außerhalb dieser Instanz der DLL gibt.
  
 **Zugriff nur durch den aktuellen Thread**
  
- Automatische Variablen im Funktionscode (einschließlich Funktionsargumenten).
    
In diesem Fall wird der Arbeitsspeicher auf dem Stapel für jede Instanz des Funktionsaufrufs beiseite gelegt.
  
> [!NOTE]
> Der Bereich des dynamisch zugewiesenen Arbeitsspeichers hängt vom Bereich des Zeigers ab, der darauf zeigt: Wenn auf den Zeiger von allen Threads zugegriffen werden kann, ist auch der Arbeitsspeicher vorhanden. Wenn es sich bei dem Zeiger um eine automatische Variable in einer Funktion handelt, ist der zugewiesene Arbeitsspeicher für diesen Thread praktisch privat. 
  
## <a name="memory-accessible-by-only-one-thread-thread-local-memory"></a>Arbeitsspeicher, auf den nur ein Thread zugegriffen werden kann: Thread-Local Speicher

Da auf statische Variablen im Textkörper einer Funktion von allen Threads zugegriffen werden kann, sind Funktionen, die sie verwenden, eindeutig nicht threadsicher. Eine Instanz der Funktion in einem Thread kann den Wert ändern, während eine andere Instanz in einem anderen Thread davon aus geht, dass es sich um etwas völlig anderes handelt. 
  
Es gibt zwei Gründe für das Deklarieren statischer Variablen innerhalb einer Funktion:
  
1. Statische Daten werden von einem Aufruf zum nächsten beibehalten.
    
2. Ein Zeiger auf statische Daten kann von der Funktion sicher zurückgegeben werden.
    
Im ersten Fall möchten Sie möglicherweise Daten haben, die beibehalten werden und für alle Aufrufe der Funktion bedeutungslos sind: vielleicht ein einfacher Indikator, der jedes Mal erhöht wird, wenn die Funktion für einen Thread aufgerufen wird, oder eine Struktur, die Nutzungs- und Leistungsdaten für jeden Aufruf sammelt. Die Frage ist, wie die freigegebenen Daten oder die Datenstruktur geschützt werden. Dies wird am besten mithilfe des kritischen Abschnitts durchgeführt, wie im nächsten Abschnitt erläutert wird.
  
Wenn die Daten nur für die Verwendung durch diesen Thread vorgesehen sind, was aus Grund 1 der Fall sein kann und immer aus Grund 2 der Fall ist, stellt sich die Frage, wie Speicher erstellt wird, der beibehalten wird, aber nur über diesen Thread zugänglich ist. Eine Lösung besteht in der Verwendung der Thread-Local Storage (TLS)-API.
  
Betrachten Sie beispielsweise eine Funktion, die einen Zeiger auf einen **XLOPER -Wert zurückgibt.**
  
```cs
LPXLOPER12 WINAPI mtr_unsafe_example(LPXLOPER12 pxArg)
{
    static XLOPER12 xRetVal; // memory shared by all threads!!!
// code sets xRetVal to a function of pxArg ...
    return &xRetVal;
}
```

Diese Funktion ist nicht threadsicher, da ein Thread die statische **XLOPER12** zurückgeben kann, während ein anderer sie überschreiben kann. Die Wahrscheinlichkeit, dass dies geschieht, ist noch größer, wenn **xlOPER12** an **xlAutoFree12 übergeben werden muss.** Eine Lösung besteht in der Zuweisung einer **XLOPER12,** der Rückgabe eines Zeigers und der Implementierung von **xlAutoFree12,** sodass der **XLOPER12-Speicher** selbst frei wird. Dieser Ansatz wird in vielen beispielfunktionen in [Memory Management in Excel verwendet.](memory-management-in-excel.md)
  
```cs
LPXLOPER12 WINAPI mtr_safe_example_1(LPXLOPER12 pxArg)
{
// pxRetVal must be freed later by xlAutoFree12
    LPXLOPER12 pxRetVal = new XLOPER12;
// code sets pxRetVal to a function of pxArg ...
    pxRetVal->xltype |= xlbitDLLFree; // Needed for all types
    return pxRetVal; // xlAutoFree12 must free this
}
```

Dieser Ansatz ist einfacher zu implementieren als der im nächsten Abschnitt beschriebene Ansatz, der auf der TLS-API basiert, hat jedoch einige Nachteile. Zunächst muss Excel **xlAutoFree** xlAutoFree12 aufrufen, unabhängig vom Typ der /   zurückgegebenen **XLOPER** /  **XLOPER12**. Zweitens gibt es beim Zurückgeben von **XLOPER** XLOPER12 s ein Problem, das den Rückgabewert eines Aufrufs einer /  C-API-Rückruffunktion darstellt. **XlOPER** XLOPER12 kann auf Arbeitsspeicher verweisen, der von Excel frei werden muss, der /   **XLOPER** /  **XLOPER12** selbst muss jedoch auf die gleiche Weise frei werden, wie er zugewiesen wurde. Wenn ein solcher **XLOPER** XLOPER12 als Rückgabewert einer XLL-Arbeitsblattfunktion verwendet werden soll, gibt es keine einfache Möglichkeit, /   **xlAutoFree** /  **xlAutoFree12** darüber zu informieren, dass beide Zeiger auf die entsprechende Weise frei gemacht werden müssen. (Das Festlegen von **xlbitXLFree** und **xlbitDLLFree** löst das Problem nicht, da die Behandlung von **XLOPER/XLOPER12s** in Excel mit beiden Satz nicht definiert ist und möglicherweise von Version zu Version geändert wird.) Um dieses Problem zu beheben, kann die XLL tiefe Kopien aller Excel **zugewiesenen XLOPER/XLOPER12s** erstellen, die an das Arbeitsblatt zurückgegeben werden. 
  
Eine Lösung, die diese Einschränkungen vermeidet, besteht im Auffüllen und Zurückgeben eines thread lokalen **XLOPER/XLOPER12-Ansatzes,** der erfordert, dass **xlAutoFree/xlAutoFree12** den **XLOPER/XLOPER12-Zeiger** selbst nicht frei gibt. 
  
```cs
LPXLOPER12 get_thread_local_xloper12(void);
LPXLOPER12 WINAPI mtr_safe_example_2(LPXLOPER12 pxArg)
{
    LPXLOPER12 pxRetVal = get_thread_local_xloper12();
// Code sets pxRetVal to a function of pxArg setting xlbitDLLFree or
// xlbitXLFree as required.
    return pxRetVal; // xlAutoFree12 must not free this pointer!
}

```

Die nächste Frage ist, wie Sie den thread-lokalen Speicher einrichten und  abrufen, d. h. wie sie die Funktion get_thread_local_xloper12 im vorherigen Beispiel implementieren. Dies erfolgt mithilfe der Thread Local Storage (TLS)-API. Der erste Schritt besteht im Abrufen eines TLS-Index mithilfe von **TlsAlloc**, der letztendlich mit **TlsFree freigegeben werden muss.** Beides wird am besten über **DllMain erreicht.**
  
```cs
// This implementation just calls a function to set up
// thread-local storage.
BOOL TLS_Action(DWORD Reason); // Could be in another module
BOOL WINAPI DllMain(HINSTANCE hDll, DWORD Reason, void *Reserved)
{
    return TLS_Action(Reason);
}
DWORD TlsIndex; // Module scope only if all TLS access in this module
BOOL TLS_Action(DWORD DllMainCallReason)
{
    switch (DllMainCallReason)
    {
    case DLL_PROCESS_ATTACH: // The DLL is being loaded.
        if((TlsIndex = TlsAlloc()) == TLS_OUT_OF_INDEXES)
            return FALSE;
        break;
    case DLL_PROCESS_DETACH: // The DLL is being unloaded.
        TlsFree(TlsIndex); // Release the TLS index.
        break;
    }
    return TRUE;
}
```

Nachdem Sie den Index erhalten haben, besteht der nächste Schritt in der Zuweisung eines Speicherblocks für jeden Thread. In [Windows Entwicklungsdokumentation](https://msdn.microsoft.com/library/ms682583%28VS.85%29.aspx) wird empfohlen, dies jedes Mal zu tun, wenn die **DllMain-Rückruffunktion** mit einem **DLL_THREAD_ATTACH-Ereignis** aufgerufen wird, und den Arbeitsspeicher für alle **DLL_THREAD_DETACH.** Wenn Sie jedoch diesen Ratschlag erhalten, würde ihre DLL unnötige Arbeit für Threads tun, die nicht für die Neuberechnung verwendet werden. 
  
Stattdessen ist es besser, eine Strategie zum Zuordnen bei erster Verwendung zu verwenden. Zunächst müssen Sie eine Struktur definieren, die Sie für jeden Thread zuordnen möchten. Für die vorherigen Beispiele, die **XLOPERs** oder **XLOPER12s** zurückgeben, reicht das Folgende aus, Aber Sie können eine beliebige Struktur erstellen, die Ihren Anforderungen entspricht.
  
```cs
struct TLS_data
{
    XLOPER xloper_shared_ret_val;
    XLOPER12 xloper12_shared_ret_val;
// Add other required thread-local data here...
};
```

Die folgende Funktion ruft einen Zeiger auf die thread-lokale Instanz ab oder weist einen zu, wenn dies der erste Aufruf ist.
  
```cs
TLS_data *get_TLS_data(void)
{
// Get a pointer to this thread's static memory.
    void *pTLS = TlsGetValue(TlsIndex);
    if(!pTLS) // No TLS memory for this thread yet
    {
        if((pTLS = calloc(1, sizeof(TLS_data))) == NULL)
        // Display some error message (omitted).
            return NULL;
        TlsSetValue(TlsIndex, pTLS); // Associate with this thread
    }
    return (TLS_data *)pTLS;
}
```

Jetzt können Sie sehen, wie der thread-lokale **XLOPER/XLOPER12-Speicher** erhalten wird: Zuerst erhalten Sie einen Zeiger auf die Threadinstanz von **TLS_data**, und dann geben Sie einen Zeiger auf den darin enthaltenen **XLOPER/XLOPER12** zurück, wie folgt. 
  
```cs
LPXLOPER get_thread_local_xloper(void)
{
    TLS_data *pTLS = get_TLS_data();
    if(pTLS)
        return &(pTLS->xloper_shared_ret_val);
    return NULL;
}
LPXLOPER12 get_thread_local_xloper12(void)
{
    TLS_data *pTLS = get_TLS_data();
    if(pTLS)
        return &(pTLS->xloper12_shared_ret_val);
    return NULL;
}

```

Die **mtr_safe_example_1** und **mtr_safe_example_2** können als threadsichere Arbeitsblattfunktionen registriert werden, wenn Sie Excel. Sie können die beiden Ansätze jedoch nicht in einer XLL kombinieren. Ihre XLL kann nur eine Implementierung von **xlAutoFree** und **xlAutoFree12** exportieren, und jede Speicherstrategie erfordert einen anderen Ansatz. Bei **mtr_safe_example_1** der an **xlAutoFree/xlAutoFree12** übergebene Zeiger zusammen mit allen Daten, auf die er verweist, frei. Bei **mtr_safe_example_2** nur die Daten mit Spitzstrichen frei.
  
Windows bietet auch eine Funktion **GetCurrentThreadId**, die die eindeutige systemweite ID des aktuellen Threads zurückgibt. Dies bietet dem Entwickler eine andere Möglichkeit, code thread sicher zu machen oder seinen Verhaltensthread spezifisch zu machen.
  
## <a name="memory-accessible-only-by-more-than-one-thread-critical-sections"></a>Nur von mehreren Threads auf Arbeitsspeicher barrierefrei: Kritische Abschnitte

Sie sollten den Lese-/Schreibspeicher schützen, auf den mehrere Threads in kritischen Abschnitten zugreifen können. Sie benötigen einen benannten kritischen Abschnitt für jeden Speicherblock, den Sie schützen möchten. Sie können diese während des Aufrufs der **xlAutoOpen-Funktion** initialisieren und lossenken und während des Aufrufs der **xlAutoClose-Funktion** auf NULL festlegen. Anschließend müssen Sie jeden Zugriff auf den geschützten Block innerhalb eines Aufrufpaars von **EnterCriticalSection** und **LeaveCriticalSection enthalten.** Es ist immer nur ein Thread in den kritischen Abschnitt zulässig. Im Folgenden finden Sie ein Beispiel für die Initialisierung, Uninitialisierung und Verwendung eines Abschnitts namens **g_csSharedTable**.
  
```cs
CRITICAL_SECTION g_csSharedTable; // global scope (if required)
bool xll_initialised = false; // Only module scope needed
int WINAPI xlAutoOpen(void)
{
    if(xll_initialised)
        return 1;
// Other initialisation omitted
    InitializeCriticalSection(&g_csSharedTable);
    xll_initialised = true;
    return 1;
}
int WINAPI xlAutoClose(void)
{
    if(!xll_initialised)
        return 1;
// Other cleaning up omitted.
    DeleteCriticalSection(&g_csSharedTable);
    xll_initialised = false;
    return 1;
}
#define SHARED_TABLE_SIZE 1000 /* Some value consistent with the table */
bool read_shared_table_element(unsigned int index, double &d)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTable);
    d = shared_table[index];
    LeaveCriticalSection(&g_csSharedTable);
    return true;
}
bool set_shared_table_element(unsigned int index, double d)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTable);
    shared_table[index] = d;
    LeaveCriticalSection(&g_csSharedTable);
    return true;
}
```

Eine andere, vielleicht sicherere Möglichkeit zum Schutz eines Speicherblocks besteht in der Erstellung einer Klasse, die eigene **CRITICAL_SECTION** enthält und deren Konstruktor-, Destruktor- und Accessormethoden sich um ihre Verwendung kümmern. Dieser Ansatz hat den zusätzlichen Vorteil, dass Objekte geschützt werden, die vor der Ausführung von **xlAutoOpen** initialisiert werden oder nach dem Aufgerufen von **xlAutoClose** erhalten bleiben. Sie sollten jedoch vorsichtig sein, wenn Sie zu viele kritische Abschnitte und den dadurch zu erstellenden Betriebssystemaufwand erstellen. 
  
Wenn Sie über Code verfügen, der gleichzeitig Zugriff auf mehr als einen Geschützten Speicherblock benötigt, müssen Sie die Reihenfolge, in der die kritischen Abschnitte eingegeben und beendet werden, sehr sorgfältig berücksichtigen. Die folgenden beiden Funktionen könnten beispielsweise einen Deadlock erzeugen.
  
```cs
// WARNING: Do not copy this code. These two functions
// can produce a deadlock and are provided for
// example and illustration only.
bool copy_shared_table_element_A_to_B(unsigned int index)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    shared_table_B[index] = shared_table_A[index];
// Critical sections should be exited in the order
// they were entered, NOT as shown here in this
// deliberately wrong illustration.
    LeaveCriticalSection(&g_csSharedTableA);
    LeaveCriticalSection(&g_csSharedTableB);
    return true;
}
bool copy_shared_table_element_B_to_A(unsigned int index)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTableB);
    EnterCriticalSection(&g_csSharedTableA);
    shared_table_A[index] = shared_table_B[index];
    LeaveCriticalSection(&g_csSharedTableA);
    LeaveCriticalSection(&g_csSharedTableB);
    return true;
}
```

Wenn die erste Funktion in  einem Thread g_csSharedTableA, während die zweite in einem anderen Thread **g_csSharedTableB,** hängen beide Threads. Der richtige Ansatz besteht in einer konsistenten Reihenfolge und beenden Sie wie folgt in umgekehrter Reihenfolge.
  
```cs
    EnterCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    // code that accesses both blocks
    LeaveCriticalSection(&g_csSharedTableB);
    LeaveCriticalSection(&g_csSharedTableA);
```

Nach Möglichkeit ist es aus Der Sicht der Threadkooperation besser, den Zugriff auf unterschiedliche Blöcke zu isolieren, wie hier gezeigt.
  
```cs
bool copy_shared_table_element_A_to_B(unsigned int index)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTableA);
    double d = shared_table_A[index];
    LeaveCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    shared_table_B[index] = d;
    LeaveCriticalSection(&g_csSharedTableB);
    return true;
}
```

Wenn es für eine freigegebene Ressource viele Streit gibt, z. B. häufige Zugriffsanforderungen für kurze Zeit, sollten Sie die Möglichkeit des kritischen Abschnitts zum Drehen in Betracht ziehen. Dies ist eine Technik, die das Warten auf die Ressource weniger prozessorintensiv macht. Dazu können Sie entweder **InitializeCriticalSectionAndSpinCount** beim Initialisieren des Abschnitts oder **SetCriticalSectionSpinCount** nach der Initialisierung verwenden, um die Anzahl der Threadschleifen vor dem Warten auf die Verfügbarheit von Ressourcen zu festlegen. Der Wartevorgang ist aufwändig, daher wird dies durch Das Drehen vermieden, wenn die Ressource in der Zwischenzeit frei wird. Bei einem Einzelnen Prozessorsystem wird die Anzahl der Drehungen effektiv ignoriert, Sie können sie jedoch trotzdem angeben, ohne schaden zu müssen. Der Speicherheap-Manager verwendet eine Drehanzahl von 4000. Weitere Informationen zur Verwendung kritischer Abschnitte finden Sie in der Dokumentation Windows SDK. 
  
## <a name="see-also"></a>Siehe auch



[Speicherverwaltung in Excel](memory-management-in-excel.md)
  
[Multithread-Neuberechnung in Excel](multithreaded-recalculation-in-excel.md)
  
[Add-In-Manager und XLL-Benutzeroberflächenfunktionen](add-in-manager-and-xll-interface-functions.md)

