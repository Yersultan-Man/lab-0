import edu.narxoz.galactic.bodies.*;
import edu.narxoz.galactic.cargo.Cargo;
import edu.narxoz.galactic.dispatcher.*;
import edu.narxoz.galactic.drones.*;
import edu.narxoz.galactic.task.*;

public class Demo {
    public static void main(String[] args) {

        Planet earth = new Planet("Earth", 0, 0, "Oxygen");
        SpaceStation iss = new SpaceStation("ISS", 100, 0, 5);

        Cargo cargo = new Cargo(50, "Food");

        DeliveryTask task = new DeliveryTask(earth, iss, cargo);

        LightDrone light = new LightDrone("LD-1", 20);
        HeavyDrone heavy = new HeavyDrone("HD-1", 100);

        Dispatcher dispatcher = new Dispatcher();

        System.out.println(dispatcher.assignTask(task, light));
        System.out.println(dispatcher.assignTask(task, heavy));
        System.out.println("Estimated time: " + task.estimateTime());
        System.out.println(dispatcher.completeTask(task));
        System.out.println("Drone status: " + heavy.getStatus());
        System.out.println("Task state: " + task.getState());
    }
}
