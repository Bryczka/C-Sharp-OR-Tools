  
OR – Tools BRYŁA Michał HUK Rafał

Or Tools jest to biblioteka stworzona przez Google, która umożliwia wykonywanie zadań optymalizacyjnych. Pomaga znaleźć optymalne rozwiązania zadań, które ze względu na ogromną liczbę rozwiązań, nie mogą być rozwiązane poprzez przeglądanie wszystkich rozwiązań. Biblioteka jest wspierana w różnych językach programowania ( C++, Python, Java, C#). Dokumentacja pozwala na zrozumienie możliwości biblioteki oraz pokazuje przykładowe implementacje różnych problemów optymalizacyjnych. 
Dokumentacja: https://developers.google.com/optimization

Pozwala na rozwiązanie problemów optymalizacyjnych takich jak:
- optymalizacja liniowa,
- optymalizacja z ograniczeniami,
- optymalizacja MILP (mieszane programowanie liniowe),
- problem pakowania (bin packing),
- przepływy w sieciach (network flows),
- optymalizacja tras przejazdów (routing),
- optymalizacja przypisania zasobów (scheduling).
Przykładowy kod rozwiązujący równanie:

// Create the linear solver with the GLOP backend.
            Solver solver = Solver.CreateSolver("SimpleLpProgram", "GLOP_LINEAR_PROGRAMMING");

            // Create the variables x and y.
            Variable x = solver.MakeNumVar(0.0, 1.0, "x");
            Variable y = solver.MakeNumVar(0.0, 2.0, "y");

            Console.WriteLine("Number of variables = " + solver.NumVariables());

            // Create a linear constraint, 0 <= x + y <= 2.
            Constraint ct = solver.MakeConstraint(0.0, 2.0, "ct");
            ct.SetCoefficient(x, 1);
            ct.SetCoefficient(y, 1);

            Console.WriteLine("Number of constraints = " + solver.NumConstraints());

            // Create the objective function, 3 * x + y.
            Objective objective = solver.Objective();
            objective.SetCoefficient(x, 3);
            objective.SetCoefficient(y, 1);
            objective.SetMaximization();

            solver.Solve();

            Console.WriteLine("Solution:");
            Console.WriteLine("Objective value = " + solver.Objective().Value());
            Console.WriteLine("x = " + x.SolutionValue());
            Console.WriteLine("y = " + y.SolutionValue());
