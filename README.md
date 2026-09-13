function dailyLog170() {
  const tasks = [
    { name: "Coding", planned: 3, completed: 3 },
    { name: "Reading", planned: 2, completed: 1 },
    { name: "Exercise", planned: 1, completed: 1 },
    { name: "Learning", planned: 2, completed: 2 }
  ];

  const plannedTotal = tasks.reduce(
    (sum, task) => sum + task.planned,
    0
  );

  const completedTotal = tasks.reduc(
    (sum, task) => sum + task.completed,
    0
  );

  const efficiency = (completedTotal / plannedTotal) * 100;

  const report = {
    date: new Date().toISOString().split("T")[0],
    plannedTasks: plannedTotal,
    completedTasks: completedTotal,
    efficiency: `${efficiency.toFixed(1)}%`,
    status: efficiency >= 80 ? "On track" : "Needs improvement"
  };

  console.log("Daily Performance Report:", report);
}

dailyLog170();
